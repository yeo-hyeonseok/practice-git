## 쓸만한 git 명령어들 모음

#### 1. 기본 브랜치를 main 브랜치로 변경하기 

`$ git config --global init.defaultBranch main`

---

#### 2. 사용자 등록

`$ git config --global user.email "이메일 주소"`<br/><br/>
`$ git config --global user.name "사용자 이름"`

---

#### 3. git 로컬 저장소 생성

`$ git init`

---

#### 4. 변경사항을 스테이징 (staging area에 저장), 커밋할 파일을 선별하는 작업

`$ git add "파일명"`
<br/><br/>
`$ git add . // 모든 파일 선택`

---

#### 5. 버전 생성

`$ git commit -m "수정 내용"`-

---

#### 6. 현재 깃 상태 확인 (종료는 q)

`$ git log`
<br/><br/>
`$ git log --all --oneline // 커밋 내역 한번에 간략하게 표시`
<br/><br/>
`$ git log --all --oneline --graph // 그래프 형식으로 보기 좋게 표시하기`

---

#### 7. 최근 커밋한 내용과 현재 파일 간의 차이점 표시 (종료는 q)

`$ git diff`
<br/><br/>
`$ git difftoll // vim 에디터로 차이 비교`
<br/><br/>
`$ git difftoll 특정 커밋 아이디 // 특정 커밋과 현재 파일 간의 차이 비교`
<br/><br/>
`$ git difftoll 특정커밋아이디 특정커밋아이디 // 특정 커밋 간의 차이 비교`

---

#### 8. 브랜치 조회

`$ git branch`

---

#### 9. 브랜치 생성

`$ git branch 브랜치이름`

---

#### 10. 브랜치 이동

`$ git switch 브랜치이름`

---

#### 11. 브랜치 병합
기준이 될 브랜치로 이동한 다음

`$ git merge 병합할브랜치이름`

---

#### 12. 브랜치 삭제

`$ git branch -d 삭제할브랜치이름 // 병합 완료된 브랜치일 경우`
`$ git branch -D 삭제할브랜치이름 // 병합 안한 브랜치일 경우`

---

#### 13. rebase로 브랜치 병합하기, 특정 브랜치의 커밋을 병합할 브랜치의 최신 커밋에다 이어 붙이는 개념, 수정내용이 많지 않은 브랜치들은 rebase를 사용하는게 로그 상 깔끔하지만 충돌이 발생할 가능성이 큼

병합시킬 브랜치로 이동한 다음 

`$ git rebase 중심브랜치이름`

중심 브랜치로 이동

`$ git merge 병합할브랜치명`

---

#### 14. squash and merge로 브랜치 병합하기

`$git merge --squash 병합할브랜치이름`

---

#### 15. 특정 파일을 최근  커밋 상태로 되돌리기

`$ git restore 파일명`

---

#### 16. 특정 커밋 시점으로 파일 되돌리기

`$ git restore --source 커밋아이디 파일명`

---

#### 17. 스테이징된 특정 파일을 되돌리기

`$ git restore --staged 파일명`

---

#### 18. 특정 커밋을 취소하기

`$ git revert 커밋아이디`

---

#### 19. 최근 커밋을 취소하기

`$ git revert HEAD`

---

#### 20. 특정 커밋 시점으로 모든 파일 되돌리기, 로그 상 아예 과거로 회귀하는 것, 협업 시에는 사용하지 않는게 좋음

`$ git reset --hard 커밋아이디`<br/><br/>
`$ git reset --soft 커밋아이디 // 되돌아가되 변동사항 지우지 말고 스테이징 시켜놓기`

---

#### 21. 기본 브랜치 이름 변경

`$ git branch -M 변경할이름`

---

####22. 로컬 저장소의 작업 내용을 원격 저장소에 저장

`$ git push -u 원격저장소주소 저장할로컬브랜치명
// -u 옵션은 주소를 기억하라는 뜻, 이후부터는 git push만 입력하면 됨`

---

#### 23. 원격 저장소 주소를 변수로 설정

`$ git remote add 변수명 원격저장소주소`

---

#### 24. 변수명 조회

`$ git remote -v`

---

#### 25. 원격저장소에 저장된 작업내용 clone해오기

`$ git clone 원격저장소주소`

---

#### 26. 원격저장소의 내용을 로컬저장소에 업데이트, pull은 fetch + merge의 개념

`$ git pull 원격저장소주소 // push 할때 -u 옵션 사용했다면 원격저장소주소 생략 가능`

---

#### 27. 현재 작업 내용 임시 저장, 최근 커밋과의 차이점을 보관하는 거임

`$ git stash`<br/><br/>
`$ git stash save '메모' // 메모도 남겨놓고 싶을 때`

---

#### 28. stash 목록 조회

`$ git stash list`

---

#### 29. 가장 최근 stash 불러오기 

`$ git stash pop`

---

#### 30. stash 삭제하기

`$ git stash drop stash번호 // 특정 stash 하나 삭제`<br/><br/>
`$ git stash clear // 모든 stash 삭제`

