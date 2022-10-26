# 백준 알고리즘 문제 추천

- 백엔드 : 이명원, 안상현, 이윤식
- 프론트 : 최윤석, 박주빈
- 풀스택 : 장정훈



## 프로젝트 소개

> 프로젝트 링크 AlgoMorgo : http://j6c204.p.ssafy.io

### 기획

![Planning](https://user-images.githubusercontent.com/74301875/197924441-67ce6bc7-fa82-44a5-a79e-d877406d077f.png)



### 간트차트

![GanttChart](https://user-images.githubusercontent.com/74301875/197924498-cf035b64-396d-4c71-88b3-3bc5f33deaf5.png)



### ERD

![erd](https://user-images.githubusercontent.com/74301875/197924522-4b3b8b18-062b-4186-ade2-c81f5ead46d9.png)



### 개발 도구

![DevTools](https://user-images.githubusercontent.com/74301875/197924540-b9ada77c-94eb-45b3-ba20-ccdf65ae702f.png)



### System Architecture

![System Architecture](https://user-images.githubusercontent.com/74301875/197924555-d9a5ceac-cb8a-4f37-9ec9-2cea5676f657.png)



### 알고리즘 소개

> 저희 문제 추천 알고리즘은 크게 다섯 단계로 구분됩니다.

![RecommendAlgorithm1](https://user-images.githubusercontent.com/74301875/197924569-1149c475-4864-4eda-b788-9098d095aa9b.png)

    1. solved.ac api를 이용하여 현재 사용자가 푼 문제들을 가져옵니다.

    2. 가져온 데이터를 활용해 각 알고리즘 별 푼 문제의 수가 담긴 배열(A)와,  푼 문제 번호가 담긴 배열(B)를 만듭니다.

    3. 정의 되어 있던 실버~플래티넘 티어 유저들의 각 알고리즘 별 푼 문제 수가 담긴 KNN 테이블(C)를 불러옵니다.

![RecommendAlgorithm2](https://user-images.githubusercontent.com/74301875/197924591-6e85466c-c6ad-42fe-b461-0f7e96cdcb83.png)

    4. 각 사용자와 방향성을 비교하기 위해 배열(A)와 테이블(C의 각 row)의 코사인 유사도를 계산하여 그 값을 배열(D)에 담습니다.

    5. 배열 D를 이용하여 최근 3일동안 추천된 문제와 겹치지 않고, 배열 B에 해당하지 않는 문제 중 방향성이 먼 사용자가 푼 일곱 문제, 방향성이 가까운 사용자가 푼 세 문제를 후보군으로 선택합니다.

    - 이 다섯 단계가 끝나고 후보로 올라온 문제 중 3문제를 사용자에게 보여줍니다.


### Swagger

- Batch Server : http://j6c204.p.ssafy.io:8081/swagger-ui/index.html
- Recommend Server : http://j6c204.p.ssafy.io:8082/swagger/
- Business Server : http://j6c204.p.ssafy.io:8083/swagger-ui/index.html

