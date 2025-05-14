# Git-Document

# 🧰 Git 명령어 정리 모음

## 📁 초기 설정 및 원격 저장소 연결
```bash
git init                                 # 현재 디렉토리를 Git 저장소로 초기화
git remote add origin [URL]             # 원격 저장소(origin) 등록
git clone [URL]                         # 원격 저장소를 복제
```

## 🔍 브랜치 관련
```bash
git branch                              # 로컬 브랜치 목록 확인
git branch -r                           # 원격 브랜치 목록 확인
git branch -a                           # 로컬 + 원격 브랜치 목록 확인
git branch [브랜치명]                   # 새 브랜치 생성
git checkout [브랜치명]                 # 브랜치 이동
git checkout -b [브랜치명]              # 새 브랜치 생성 후 이동
git branch -d [브랜치명]                # 로컬 브랜치 삭제
git push origin --delete [브랜치명]     # 원격 브랜치 삭제
```

## ⬆️ 변경 사항 업로드
```bash
git add .                               # 전체 변경 파일 스테이징
git commit -m "커밋 메시지"             # 커밋 생성
git push origin [브랜치명]              # 원격 저장소로 푸시
```

## ⬇️ 변경 사항 받기
```bash
git pull                                # 원격 저장소에서 최신 변경 사항 가져오기
```

## 🔄 상태 확인 및 기타
```bash
git status                              # 변경된 파일 상태 확인
git log                                 # 커밋 로그 확인
git switch [브랜치명]                   # 브랜치 전환 (checkout 대체 가능)
```

## 📌 GitHub Issue와 연결
- 커밋 메시지 또는 PR 메시지에 `#이슈번호` 를 넣으면 해당 이슈와 자동 연결됩니다.
  ```bash
  git commit -m "feat: 더하기 기능 구현 #2"
  ```
