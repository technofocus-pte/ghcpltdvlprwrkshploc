**실습 14: 리포지토리의 공급 체인을 보안하기**

목표:

다양한 타사 종속성에 의존하는 소프트웨어 프로젝트의 보안을 유지할 책임이
있습니다. 프로젝트 공급망의 무결성과 안전을 보장하려면 이러한 종속성을
효과적으로 이해하고 관리하는 것이 중요합니다. 여기에는 종속성 내의
잠재적인 취약점을 식별하고 프로젝트를 보호하는 데 필요한 패치를 적용하는
것이 포함됩니다. 이 실습에서는 GitHub의 종속성 그래프 기능을 사용하여
종속성을 모니터링하고 검토하여 프로젝트가 안전하고 최신 상태로
유지되도록 하는 방법을 배웁니다.

이 실습에서는 다음을 수행할 것입니다:

- 종속성 그래프 활성화: 리포지토리 설정에서는 종속성 그래프 기능을
  활성화하고 확인하여 프로젝트의 종속성을 시각화하기

- 새 종속성 추가: 프로젝트에 새 종속성을 추가하고 제대로 통합되었는지
  확인하기

- 종속성 그래프 검토: 종속성 그래프를 사용하여 새 종속성이 올바르게
  반영되고 모니토링되는지 검토하고 확인하기

연습 01: 새 리포지토리를 생성하기

1.  다음 링크로
    이동하세요: <https://github.com/skills/secure-repository-supply-chain>

이 실습에서는 공개 템플릿 **skills-secure-repository-supply-chain**을
사용하여 리포지토리를 생성할 것입니다

![](./media/image1.jpeg)

2.  **Use this template** 메뉴에서 **Create a new repository**를
    선택하세요.

![](./media/image2.jpeg)

3.  다음 세부 정보를 입력하고 **Create Repository**를 선택하세요.

    - 리포지토리 이름: **skills-secure-repository-supply-chain**

    - 리포지토리 유형: **Public**

![](./media/image3.jpeg)

연습 02: 종속성 그래프가 사용하도록 설정되어 있는지 확인하기

1.  새로 생성한 리포지토리의 랜딩 페이지에서 **Settings** 탭으로
    이동하세요.

![](./media/image4.jpeg)

2.  **Settings** 페이지에서 **Security**에서 사용 가능한 **Code security
    and analysis**을 선택하세요.

![](./media/image5.jpeg)

3.  종속성 그래프를 확인/활성화하세요. (리포지토리가 비공개인 경우
    여기에서 활성화하고 리포지토리가 공개인 경우 기본적으로
    활성화됩니다.)

![](./media/image6.jpeg)

연습 03: 새 종속성 추가 및 종속성 그래프 보기

1.  **Code** 탭으로 이동하고 **code/src/AttendeeSite** 폴더를 찾으세요.

**참고:** 폴더를 찾아보거나 **Go to file** 검색 code/src/AttendeeSite를
사용할 수 있습니다

![](./media/image7.jpeg)

![](./media/image8.jpeg)

2.  **package-lock.json** 파일을 여세요.

![](./media/image9.jpeg)

![](./media/image10.jpeg)

3.  \# 14 행과 \# 15 행 사이에 다음 코드 조각을 삽입하세요.

4.  "follow-redirects": {

5.  "version": "1.14.1",

6.  "resolved":

7.  "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",

8.  "integrity":

9.  "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="

},

![](./media/image11.jpeg)

**참고:** 추가된 코드 조각이 스크린샷과 같이 제대로 들여쓰기되었는지
확인하세요

10. 오른쪽 상단의 **Commit changes**를 클릭하세요.

![](./media/image12.jpeg)

11. 기본 탐색 바에서 **Insights tab**을 클릭하세요.

![](./media/image13.jpeg)

12. On the left side navigation pane click on the **Dependency graph**.

![](./media/image14.jpeg)

13. 종속성 허브에서 모든 새 종속성을 검토하세요.

![](./media/image15.jpeg)

14. follow-redirects를 검색하고 방금 추가한 새 종속성을 검토하세요.

![](./media/image16.jpeg)

요약:

이제 프로젝트의 종속성을 관리하고 리포지토리의 공급만을 보호하는 데 대한
귀중한 통찰력을 얻어 보안 위험을 사전에 해결하고 완화할 수 있습니다.
