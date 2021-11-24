cd geometric_lib
git checkout develop
git checkout release
git log --graph --all
git checkout main
git merge develop --no-ff
git log --graph --all
git reset --hard HEAD^
git log --graph --all
git merge develop --ff
git log --graph --all
git config --global merge.tool meld
git checkout release
git rebase -i main
git mergetool
git rebase --continue
git mergetool
git rebase --continue
git log --all --pretty=oneline --graph
git checkout main 
git merge release --ff
git log --pretty=oneline --graph 