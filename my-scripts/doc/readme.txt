1) create a new repo on github

git clone git@github.com:RobertBerger/linux-yocto.git

2) add my-scripts dir

cd linux-yocto

echo "# linux-yocto fork" >> README.md

git init

git add .

git commit -m "first commit"

git push -u origin master

3) use my repo

mv linux-yocto linux-yocto.ori
git clone git@github.com:RobertBerger/linux-yocto.git

4) add upstream

cd linux-yocto

git remote add official-upstream https://git.yoctoproject.org/linux-yocto

$ git fetch official-upstream

git fetch official-upstream
warning: no common commits
...

5) use specific upstream branch and make our own branch

git checkout -b v6.18/standard/phyboard-pollux-imx8mp-3 official-upstream/v6.18/standard/base
git checkout -b v6.18/standard/pollux official-upstream/v6.18/standard/base
