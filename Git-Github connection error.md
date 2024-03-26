# issue
vscode의 Default branch 이름이 master로 되있어서 push 오류가 계속 발생. 

# solution
vscode에서 branch 이름을 바꾼다. 
- git branch -m master main 

# 외에 알아두면 좋은 git command 

``` cpp
// 깃 저장소 생성 
git init 

// Working directory -> Staging Area 
git add [directory]
git add . 

// Staging Area -> repository(.git)
git commit -m " " 

// connect with remote repository
git remote add origin [address]

// change branch name
git branch -M [branch name]
git branch -m [present] [after]

// (option) README.md가 있다면: do pull before push
git pull origin [branch name]

// local repository -> remote repository
git push -u origin [branch name]

// after file modification & add: next commit & push
git pull origin [branch name] (option: if you didn't work at other directory, you don't need to do it)
git add [directory]
git commit -m ""
git push -u origin [branch name]
```
