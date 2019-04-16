# FreeThrow
# Git Convention

## 1. Commit

### 1.1 Commit Type

+ Type
  + 코드에 관련된 Type
    + feat : 새로운 기능
    + refactor : 기능 수정(보완)
    + fix : 버그 수정
    + test : test 코드 추가 및 수정

  + 그 외에 관련된 Type

    + docs : 새로운 문서 혹은 문서 수정
    + style : 코드 의미에 영향이 없는 것이 변경(예: 띄어쓰기, 들여쓰기,  세미콜론 등)
    + chore : 소스나 테스트 파일, style 이외의 것 변경
    + revert : 이전의 commit으로 되돌아 감

+ 사용

  + 사용 양식

    > type : 한 줄 요약
    >
    > 변경사항 설명
    >
    > Resolves : 이슈관리대장 번호
    >
    > See also : 관련 이슈 번호

  + 사용 예

    > feat : 로그인 기능 commit
    >
    > 
    >
    > MemberDAO, MemberDAOImpl : 메소드(findMemberById, login) 추가
    >
    > login_fail : 로그인 실패시 alert을 위한 view 추가
    >
    > 
    >
    > Resolves : #1
    >
    > See alse : #2, #3



### 1.2 이슈관리 대장 등록

+ 제목 : 첫 번째는 Type으로 구분

  + Type 종류

    + feat : 기능
    + error : 에러 발생 공유
      - error관련 이슈는 상황을 자세히 설명 = 자신이 어떻게 코드를 작성했는지 설명
      - error 해결 시 댓글로 해결방법 작성
    + conflict : commit, push, merge 등 git에 대한 이슈등록
    + etc : 그 외
    + 종류는 타협으로 더 추가 가능

+ 사용 예

  + > [feat] 로그인 기능 구현

    

  + > [error] ID 중복체크를 위한 Ajax에서 오류
    >
    > > ajax 사용을 위해 아래와 같이 작성
    > >
    > > type : "get",
    > >
    > > url : "/idCheckAjax"
    > >
    > > data : "id="+$("#id").text(),
    > >
    > > success:function(result){
    > >
    > >    (생략)
    > >
    > > }
    > >
    > > 
    > >
    > > //해결 한 후 댓글
    > >
    > > > data : "id="+$("#id").text() 에서 text()가 아닌 val()로 변경
