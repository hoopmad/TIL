# Mentoring Day 1

> 2023년 4월 8일 토요일

# GPT (Generative Pre-trained Transformer)

> 대량의 데이터로 다양한 작업을 수행할 수 있도록 사전 학습한 Transformer 모델

## 실행 단계
1. Collect demonstration data and train a supervised policy
2. Collect comparision data and train a reward model
3. Optimize 

## ChatGPT
- GPT-3.5
- GPT-4

## 프로젝트 피드백

1. 프로젝트의 정체성
   1. 냉장고와 모바일 냉장고의 연계 시스템
   2. 유통(소비)기간 알림
      1. 냉장고 안에서 오래 잠들어 있는 식품
2. 현실적인 어려움
   1. 실제로 사람들이 수기로 일일이 기록할까?
   2. 레시피 추천 기능 구현
3. 프로토타입을 만드는 과정
4. 데이터 파이프라인을 만드는 과정의 중요성
   1. 전체의 70-80%
   2. AWS 협업
5. 사진에서 재료를 구분
   1. 재료의 개수와 무게
      1. 레시피를 추천하기 위해선 무게가 필요할 수도
      2. 재료를 구분하는 방법의 어려움

## 데이터베이스 피드백
1. 차원(dimension)테이블과 이력(fact)테이블의 분리
2. 중복을 허용할 것인가?
   1. 허용하면 빠른 속도
   2. 허용하지 않으면 공간 절약
3. 회원과 냉장고 join이 너무 빈번
   1. 두개를 합친 테이블을 미리 만드는 방법
   2. 역정규화
4. 스타스키마
   1. Fact table이 가운데 오는 형식
   2. 주변에 dimension 테이블
5. 왜래키 constraint 제거
   1. 회원id가 없어도 데이터가 들어가게

### 추가 질문
1. 회원이 탈퇴하면?
   1. 삭제 전 flag를 통해 탈퇴한 회원 표시
   2. 새벽에 batch 프로그램이 돌면서 삭제 플래그가 y인 것들만 삭제 후 아카이빙