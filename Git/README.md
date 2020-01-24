# Git 명령어 사용법

## Git User Setting - [Git 사용자 설정]

```
// 전역 사용자명 / 이메일 설정
git config - -global user.name “Your name”
git config - -global user.email “Your email address”

// 특정 저장소 사용자명 / 이메일 설정
cd ./{repository name}
git config user.name “Your name”
git config user.email “Your email address”
```

## Compare Remote Repository - [원격 저장소와 로컬 저장소 변경사항 비교]

```
git fetch
git pull // 변경 사항 적용
```

## Create Repository - [저장소 생성]

```
mkdir {repository name}
cd {repository name}
git init
```

## Clone Repository - [저장소 복제]

```
git clone {repository url}

git clone --depth 200 {repository url} // 마지막 20개의 커밋만 포함 복제
```

## Code Commit - [코드 기록]

```
git add {file}
1) git commit -m "input comment"
2) git commit -m "title comment" -m "description comment"
```

## Code Commit Cancle - [코드 기록 취소]

```
git reset HEAD {file}
```

## Code Commit Message Edit - [코드 기록 수정]

```
git commit --amend
```

## Push Repository - [저장소 올리기]

```
git push
```

## Show Branch List - [브랜치 확인]

```
git branch // Local Branch
git branch -r // Remote Branch
git branch -a // Both Branch
```

## Create Branch - [브랜치 생성]

```
git branch {branch name}
git checkout -b {branch name} // 브랜치 생성 & 브랜치 전환
git branch -m {original branch} {branch name} // 브랜치 이름 변경
```

## Change Branch - [브랜치 전환]

```
git checkout {branch name}
```

## Drop Branch - [브랜치 삭제]

```
// Drop Local Branch
git branch -d {branch name}

// Drop Remote Branch
1) git branch -d {branch name}
git push {remote name} {branch name}

2) git push {remote name} :{branch name}
```

## Check Commit Info - [커및 정보 보기]

```
git blame {file name}
```