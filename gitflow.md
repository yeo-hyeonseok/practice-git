## GitFlow 방식

안정적인 버전별 배포가 가능하나 CI/CD에는 부적합, 상황에 따라 변형해도 됨

### main 
>*배포용*

원본 브랜치

### develope 
>*from **main** / to **main***

개발용 브랜치, main 브랜치의 사본

### feature/~
>*from **develope** / to **develope***

기능 단위의 브랜치, 새로운 기능 추가하려면 feature 브랜치 파서 작업하면 됨, develope 브랜치에서 분기

### release
>*from **deveope** / to **develope** / to **main*** 

main 브랜치에 병합 전 여러가지 테스트해보는 임시 브랜치

### hotfix/~
> *from **main** / to **develope** / to **main***

버그 발생 시 사용하는 브랜치
