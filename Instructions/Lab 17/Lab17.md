**실습 17: GitHub 리포지토리에서 비밀 검사를 사용하도록 설정하고 토큰을
커밋하기**

공유 GitHub 리포지토리를 사용하여 팀 프로젝트를 진행하는 소프트웨어
개발자입니다. 코드를 안전하게 유지하고 우발적인 유출 방지를 위해 실수로
리포지토리에 커밋될 수 있는 API 토큰이나 암호와 같은 민감한 정보를
식별하는 ㅔ 도움이 되는 기능인 비밀 검사---를 구현하기로 결정했습니다.

목표:

이 실습에서는 다음을 수행할 것입니다:

1.  비밀 검사 활성화: GitHub 리포지토리에서 비밀 검사를 구성하여 중요한
    정보를 자동으로 검색하고 플래그를 지정하기

2.  토큰 커밋: 비밀 검사 기능의 효과를 테스트하기 위해 의도적으로
    리포지토리에서 토큰 또는 기타 중요한 정보를 추가하기

연습 \#1: GitHub 리포지토리 생성하고 비밀 검사 활성화하기

작업 \#1: 템플릿에서 리포지토리를 생성하기

1.  GitHub 계정으로 로그인하세요.

2.  다음 링크로
    이동하세요: https://github.com/skills/introduction-to-secret-scanning

이 실습에서는 공개 템플릿 "**skills-introduction-to-secret-scanning**"을
사용하여 리포지토리를 생성할 것입니다.

![](./media/image1.jpeg)

3.  **Use this template** 메뉴에서 **Create a new repository**를
    선택하세요.

![](./media/image2.jpeg)

4.  다음 세부 정보를 입력하고 **Create Repository**를 선택하세요.

    - 리포지토리 이름: **skills-introduction-to-secret-scanning**

    - 리포지토리 유형: **Public**

![](./media/image3.jpeg)

작업 \#2: 비밀 스캐닝 활성화하기

1.  새로 생성한 리포지토리의 랜딩 페이지에서 위쪽 탐색
    모음에서 **Settings**을 선택하세요.

![](./media/image4.jpeg)

2.  사이드바의 **Security** 섹션에서 **Code security and analysis**를
    선택하세요.

**참고**: **Security** 메뉴를 보려면 아래로 스크롤하야 합니다

![](./media/image5.jpeg)

3.  페이지 하단으로 스크롤하여 비밀 검사를 위한 **Enable**를 클릭하세요.

**참고:** **Disable** 버튼이 표시되면 리포지토리에 대해 비밀 검사가 이미
활성화로 설정되어 있음을 의미합니다.

![](./media/image6.jpeg)

아직 활성화되지 않은 경우 아래와 같이 **Enable** 버튼이 표시됩니다:

![](./media/image7.jpeg)

**참고:** 비밀 스캔이 활성화되면 리포지토리의 자격 증명에 대한 이메일
알림이 계정과 연결된 메일 ID로 전송됩니다. 이 스킬 리포지토리의 토큰은
비활성화됩니다. 환경에 대한 위험은 없습니다.

이제 리포지토리에서 비밀 검사를 활성화로 설정했으므로 새 토큰을 커밋하여
작동 방식을 살펴보겠습니다.

연습 \#2: 토큰 커밋하기

이 연습에서는 AWS 키와 액세스 ID를 리포지토리에 커밋합니다. AWS에
로그인하는 데 사용할 수 없는 비활성 토큰입니다.

1.  기본 탬색 모음의 왼쪽 상단 창에서 **Code** 탭을 클릭하고
    **credentials.yml** 파일을 선택하세요.

![](./media/image8.jpeg)

2.  오른쪽의 Edit 버튼을 클릭하세요.

![](./media/image9.jpeg)

3.  다음 텍스트를 복사하여 **credentials.yml** 파일의 편집 창에 있는
    기존 코드 아래에 붙여넣으세요.

4.  default:

5.  aws_access_key_id: AKIAQYLPMN5HNM4OZ56B

6.  aws_secret_access_key: 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

7.  output: json

region: us-east-2

![](./media/image10.jpeg)

8.  오른쪽 상단 모서리에 있는 **Commit changes** 버튼을 클릭하고
    **Commit Changes** 창에서 **Commit Changes** 를 다시 클릭하세요.

![](./media/image11.jpeg)

**참고:** 변경 내용을 커밋하면 GitHub 계정과 연결된 사서함에 경고가
표시됩니다.

![](./media/image12.jpeg)

요약:

이제 코드와 데이터를 보호하기 위해 비밀 검사를 활성화하고 테스트하는
방법에 대한 실질적인 이해를 얻었습니다.
