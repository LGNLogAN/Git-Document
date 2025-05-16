# Git-Document

# 🧰 Git 명령어 정리 모음

## 📁 초기 설정 및 원격 저장소 연결
```bash
git init                                 # 현재 디렉토리를 Git 저장소로 초기화
git remote add origin [URL]             # 원격 저장소(origin) 등록
git clone [URL]                         # 원격 저장소를 복제
```

## 🕰️ 지정된 커밋시점으로 되돌리기
```bash
git log --oneline
git reset --hard [Hash 값]
git push origin [브랜치] --force
```

## ✏️ 특정 커밋 삭제
```bash
git log --oneline
git rebase -i [지우고싶은 이전 커밋 코드값]
i 눌러 편집모드로 진입
pick -> drop 변경
esc -> :wq! -> enter
git push origin [커밋삭제한 브랜치] --force ( 강제 푸쉬 )
```

## 🔍 브랜치 관련
```bash
git branch                              # 로컬 브랜치 목록 확인
git branch -r                           # 원격 브랜치 목록 확인
git branch -a                           # 로컬 + 원격 브랜치 목록 확인
git branch [브랜치명]                   # 새 브랜치 생성
git fetch origin                        # 원격 저장소에 있는 브랜치 가져오기
git checkout [브랜치명]                 # 브랜치 이동
git checkout -b [브랜치명]              # 새 브랜치 생성 후 이동
git branch -d [브랜치명]                # 로컬 브랜치 삭제
git push origin --delete [브랜치명]     # 원격 브랜치 삭제
git remote prune origin                 # 원격 저장소에서 존재하지않는 로컬의 origin/ 경로의 브랜치를 삭제
```

## ⬆️ 변경 사항 업로드
```bash
git add .                               # 전체 변경 파일 스테이징
git commit -m "커밋 메시지"             # 커밋 생성
git push origin [브랜치명]              # 원격 저장소로 푸시
```

## 🔄 상태 확인 및 기타
```bash
git status                              # 변경된 파일 상태 확인
git log                                 # 커밋 로그 확인
git switch [브랜치명]                   # 브랜치 전환 (checkout 대체 가능)
```

## 📌 저장소 연결 순서 1
```bash
git init                            # 깃 파일 생성
git remote add origin [저장소URL]   # 원격 저장소 연결
git fetch origin                    # 원격 브랜치 모두 불러오기 ( origin / * )
or
git pull origin main                # 메인 브랜치 풀
git branch -m master main           # 메인 브랜치 풀 시 master 로 변경될 때 사용
git switch [브랜치명]               # 원격 브랜치 로컬로 전환하기
```

## 📌 저장소 연결 순서 2
```bash
git clone [저장소URL]
git branch -r
git checkout [브랜치명]
or
git checkout -b [브랜치명]
```


