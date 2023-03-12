# 23-Project1-R
# 602377106 김준태

GIT 설치, CMD창에서 git -v 또는 git --version으로 설치 확인
VS Code 설치, 실행 후

### 사용자 정보 등록 (공유 PC는 --global 옵션 제거 권장)
* git config --global user.name “zzonvk"
* git config --global user.email "zzonvk@naver.com"

### 설정 내용 확인
* git config --global user.name
* git config --global user.email

### VsCode GiHub 연동

1. 폴더를 연후, 소스 제어의 Initialize Repository를 클릭

2. 터미널에 git 초기화된 폴더 에 파일을 생성하거나
변경 사항이 발생 하면 소스 제어에 바뀐 파일만큼의 숫자가 표시.

3. test 파일 만들기
* 실무프로젝트 첫 번째 모듈 생성.

4. 메시지라고 하는 곳에 커밋 제목과 설명을 작성. 메세지의 경우 제목을 적고 50글자 이내로 작성.
엔터키를 두번 누른 후 설명을 작성한다.

5. 변경된 내용 중 일부 파일만 푸시하는 경우 케밥 메뉴를 클릭하고 '푸시'를 선택하면 GitHub에 아직 Repository가 시작되기 전에 Add Remote(원격지점 추가) 버튼을 클릭한 후 원하는 레포지토리를 선택.

6. 변경된 내용을 모두 푸시하는 경우 더 이상의 수정될 파일이 없을시 커밋 버튼이 '게시 branch'으로 보임.
현재 작업 폴더와 같은 이름으로 원격에 생성

- public을 선택 시 다른 사용자가 해당 내용을 볼 수 있게 됨 private의 경우 비공개이므로 다른 사용자가 볼수 없음

7. 기본 브라우저로 GitHub에 플러그인 후
status bar의 구름 아이콘(게시 branch)을 클릭하거나 푸시 시 팝업창에서 VS Code와 GitHub를 연동.


### R언어
* R은 통계를 포함한 데이터 분석 작업에 특화된 언어.

