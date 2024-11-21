git clone https://github.com/angel-022/angel.git
cd angel
echo "angel" > README.md
git add README.md
git commit -m "add readme file"
git push 
git checkout -b master
mkdir Task1 
echo "add readme to Task1 on the master branch" > Task1/README.md
git add .
git commit -m "adding readme to task1"
git push --set-upstream oirgin master
git checkout -b dev 
touch test
git add test
git commit -m "add this file to the dev branch"
git push --set-upstream origin dev
git checkout -b %USERNAME-new_feature
echo "add readme to the %USERNAME-new_feature" > README.me
echo ".*" > .gitigrore
git add -f README.md .gitignore
git commit -m "adding .gitignore and readme.md to %USERNAME-new_feature"
git push --set-upstream origin %USERNAME-new_feature
git checkout dev
git pull 
git merge %USERNAME-new_feature 
git commit -m "merge %USERNAME-new_feature to the dev branch"
git push origin dev
git checkout master
git merge dev 
git commit -m "merge dev with master branch"
git push origin master
git checkout %USERNAME-new_feature
echo "this is the new readme" > README.md
git commit -m "edit the readme file in the %USERNAME-new_feature"
git revert HEAD
git commit -m "Revert last commit"

git checkout master
git log > log.txt
git commit -m "add git log output to log.txt on the master branch"
git push 
git branch -d %USERNAME-new_feature
git push origin --delete %USERNAME-new_feature
git fetch --prune
