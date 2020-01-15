# RNASeq
curl -LOk https://github.com/ewels/MultiQC/archive/master.zip
unzip master.zip
cd MultiQC-master
python setup.py install
git clone https://github.com/ewels/MultiQC.git
cd MultiQC
python setup.py install
git remote add origin https://github.com/ewels/MultiQC
git config gc.auto 0
git config --get-all http.https://github.com/ewels/MultiQC.extraheader
git -c http.extraheader="AUTHORIZATION: basic ***" fetch --tags --prune --progress --no-recurse-submodules origin +refs/heads/*:refs/remotes/origin/* +refs/pull/1089/merge:refs/remotes/pull/1089/merge
