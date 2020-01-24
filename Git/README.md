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

## Create Repository - [저장소 생성]

```
mkdir {repository name}
cd {repository name}
git init
```

## Clone Repository - [저장소 복제]

```
git clone {repository url}

// Example
git clone https://github.com/Mineru98/Usage_Collection
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