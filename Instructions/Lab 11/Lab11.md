**실습 11: 워크플로우를 재사용 가능하게 생성하고 매트릭스 전략을
사용하여 여러 버전의 노드을 실행하기**

목표:

빌드, 테스트 및 배포와 같은 작업에 대한 공통 워크플로우를 공유하는
프로젝트 내에서 여러 리포지토리를 관리하고 있습니다. 중복성을 방지하고
이러한 리포지토리 간게 일관성을 유지하려면 GitHub Actions을 사용하여
재사용 가능한 워크플로우를 구현하기로 결정합니다. 워크플로우 호출
트리거를 활용하면 워크플로우 구성을 중앙 집중화하여 변경 사항이 한
곳에서 이루어지고 모든 관련 리포지토리에 자동으로 적용되도록 할 수
있습니다. 또한 매트릭스 전략을 활용하여 여러 버전의 Node.js로
워크플로우를 테스트하고 호환성과 확장성을 향상시킵니다.

이 실습에서는 다음을 수행할 것입니다:

- workflow_call 트리거를 사용하여 여러 리포지토리에서 워크플로를
  재사용할 수 있도록 하여 구성 중복성을 줄이기

- 리포지토리로 이동하여 workflow_call 트리거를 포함하도록 워크플로
  파일을 업데이트하고 변경 사항을 커밋하기

- 풀 리퀘스트를 생성하고 변경 내용과 예외를 비교하기

연습 \#1: 새 리포지토리를 생성하기

1.  다음 링크로 이동하세요: https://github.com/skills/reusable-workflows

이 실습에서는 공개 템플릿 "**skills-reusable-workflows**"를 사용하여
리포지토리를 생성할 것입니다.

![](./media/image1.jpeg)

2.  **Use this template** 메뉴에서 **Create a new repository**를
    선택하세요.

![](./media/image2.jpeg)

3.  다음 세부 정보를 입력하고 **Create Repository**를 선택하세요.

    - 리포지토리 이름: **skills-reusable-workflows**

    - 리포지토리 유형: **Public**

![](./media/image3.jpeg)

연습 \#2: 워크플로우에 workflow_call 트리거를 추가하기

1.  새로 생성한 리포지토리의 랜딩 페이지에서 **Code** 탭으로
    이동하세요\*\*.\*\*

![](./media/image4.jpeg)

2.  main 분기 드롭다운에서 **reusable-workflow** 분기를 선택하세요.

![](./media/image5.jpeg)

3.  분기를 변경한 후 **.github/workflows/** 폴더로 이동한 후
    **reusable-workflow.yml** 파일을 선택하세요.

![](./media/image6.jpeg)

![](./media/image7.jpeg)

4.  **reusable-workflow.yml** 파일 편집기에서 **Edit in place**를
    선택하세요.

![](./media/image8.jpeg)

5.  **workflow_dispatch** 이벤트 트리거를 **workflow_call** 이벤트
    트리거로 바꾸고 **Commit changes**를 클릭하세요.

**참고**: **줄 \#3**에서 **줄 \#8**까지의 코드 블록을 아래 블록으로
바꾸세요

on:

workflow_call:

inputs:

node:

required: true

type: string

![](./media/image9.jpeg)

6.  **Commit changes**창에서 **Commit changes**를 클릭하세요.

![](./media/image10.jpeg)

연습 \#3: 이전 연습에서 변경한 내용을 확인하려면 풀 리퀘스트를 생성하기

1.  **Pull requests** 탭에서 **New pull request**를 클릭하세요.

![](./media/image11.jpeg)

2.  **Comparing changes page**에서 **base**를 **main**로
    설정하고 **compare**를 **reusable-workflow**로 설정하세요.

![](./media/image12.jpeg)

3.  **Open a pull request** 페이지에서 **Create pull request**를
    클릭하세요.

![](./media/image13.jpeg)

4.  작업이 실행될 때까지 20초 동안 기다렸다가 결과를 검토하세요.

요약:

이제 GitHub Actions를 사용하여 효율적인 재사용 가능한 워크플로우를
생성하고 다양한 환경에 맞게 최적화하는 실무 경험을 쌓았습니다.
