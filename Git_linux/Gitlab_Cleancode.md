# Gitlab_CI  

CI-continuous Integration  
: 새로운 코드에 대한 변경사항이 꾸준히 자동으로 빌드 및 테스트 되어 여러 개발자가 동시에 작업할 때 인터럽트가 발생하는 것을 방지 가능  
: 자동으로 (빌드 - 테스트 - 머지)를 해줌  

CI가 없으면 개발자가 코드 작성 - 빌드 - 테스트 - 배포까지 다 해주어야 함  
**CI를 한번만 잘 작성해놓으면 개발자는 코드만 작성하면 됨**  
```  
## CI하지 않고 빌드하기  
npm install express  # express로 어플을 하나 만듬  
npm install --save-dev mocha should supertest  
```  
Heroku : CI 없이 배포를 위한 사이트   

## CI로 자동화 시키기  

1. .gitlab-ci.yml 파일을 다음과 같이 저장한다.   
![image](https://user-images.githubusercontent.com/74280650/123088605-e8a4de80-d460-11eb-9acf-7187bf22ec56.png)  

2. 이를 Git lab에 push하면 자동으로 Git lab이 test 코드를 돌려줌  

3. 실제 프로젝트에 CI적용 시 다음과 같이 진행함  
  - Unprotected branch 에 Push 할 때  
  : test 및 lint 진행  
  - Protected branch에 MR 할 때  
  : test 및 lint 진행, 실패 시 Merge 불가  
  - PRotected branch에 Push / Merge 할 때  
  : test 및 lint 진행, 성공시 deploy  
  
4. Git lab - Settings - General로 이동
  : Merge checks -> pipelines must succeed 체크   
  : **이를 통해 CI를 Pass하지 못한 경우 Merge 할 수 없도록 설정 가능**    
  
## Gitlab_Wiki  
: 프로젝트의 내용을 이해하기 쉽게 설명 작성 가능  
: 해당 문구에 링크 작성 가능    

## Member 권한과 접근  
: 멤버 탭에서 멤버를 설정  
: 서브그룹을 설정 가능  
: 서브 그룹과 프로젝트는 상위 그룹의 멤버를 상속한다.  
: 그룹을 한 번에 초대할 때만 Max Access Level을 넘지 못한다.  
: 그룹 아래에 추가적으로 서브 그룹을 계속 생성할 수 있다.  

## Lint  
: 프로그램 실행에 문제 생길 여지가 적지만, 나중에 문제될 수 있는 자잘한 문제들을 표시  
: '' or "" 통일 여부나 누락된 세미콜론 찾기 등  

```  
Npm install --save-dev eslint  # eslint 프로그램 설치  
./node_modules/.bin/eslint .--init # 세부사항 설정  
./node_modules/.bin/eslint .--fix # 세부사항 틀린 부분 고치기  
```  
  
![image](https://user-images.githubusercontent.com/74280650/123106360-8a352b80-d473-11eb-9a35-5aae3b7bd62f.png)  
 이런 식으로 스테이지 추가 가능  

## Gitlab_통계  
: Analytics 탭 사용  

## Gitlab_Operations  
Metrics : 메모리 사용량 확인  
Environment -> Deploy : roll-back 가능 (원하는 커밋에서 새로고침 버튼을 누르면 됨)  

## Gitlab_Error Tracking  
: 배포된 서비스에서 발생하는 Error에 대한 정보를 추적하기 위해 Gitlab에서 제공하는 기능  

## Gitlab_Feature flags  
: 특정 기능을 껏다 켰다 할 수 있음  

# Visual Studio Code 단축키  
```컨트롤 + 쉬프트 + 슬래쉬``` : 기본 주석  
```컨트롤 + 알트 + A``` : 블록 주석  
```컨트롤 + 쉬프트 + P``` : 에디터 제공 명령어들을 검색 가능  

# Code smeell~  

1. 긴 메서드  (어떠한 작업을 하는지 명확하도록)  
2. 중복 코드  (쓸데없이 늘어나는 코드 길이)  
3. 긴 매개변수 목록  (일관성이 떨어짐)  
4. 너무 많은 주석  (좋은 네이밍이 훨씬 나음)  
5. 전역 변수  (예상치 못한 오류 발생 가능)  
6. 게으른 클래스  (재사용할 수 없는 클래스는 그것을 유지하고 이해하는 비용이 듦)
7. 거대한 클래스  (너무 크게 만들면 안됨)  

# 띵언 모음  
**C++ 창시자, 비야네 스트롭스트룹(Bjarne Stroustrup)**  
클린 코드는 단순하고 직접적이다. 클린 코드는 잘 쓴 문장처럼 읽힌다. 클린 코드는 결코 설계자의 의도를 숨기지 않는다. 오히려 명쾌한 추상화와 단순한 제어문으로 가득하다.  

**객체지향의 대가, 그래디 부치(Grady Booch)**  
나는 우아하고 효율적인 코드를 좋아한다. 논리가 간단해야 버그가 숨어들지 못한다. 의존성을 최대한 줄여야 유지보수가 쉬워진다. 오류는 명백한 전략에 따라 철저히 처리한다. 성능을 최적으로 유지해야 사람들이 원칙 없는 최적화로 코드를 망치려는 유혹에 빠지지 않는다. 클린 코드는 한 가지를 제대로 한다.  

**『레거시 코드 활용 전략』 저자, 마이클 페더스(Michael Feathers)**  
클린 코드의 특징은 많지만, 그중에서도 모두를 아우르는 특징이 하나 있다. 클린 코드는 언제나 누군가 주의 깊게 짰다고 느끼게 한다. 고치려고 살펴봐도 딱히 손댈 곳이 없다. 작성자가 이미 모든 사항을 고려했으므로, 고칠 궁리를 하다 보면 언제나 제자리로 돌아온다. 그리고는 누군가 남겨준 코드, 누군가 주의 깊게 짜놓은 작품에 감사를 느낀다.  























  

  


