# Design-and-Project-Deepening-I---Reverse-design
시각장애인을 위한 웹쇼핑몰 개발 및 연구

## 🗓️ 개발 기간

2021/3/16 ~ 2021/3/30

## 📜서비스 내용

- 문제 제기
    - 시각장애인의 인터넷 쇼핑의 이용 실태를 살펴보니 상세 정보가 이미지 파일에 담겨 있는 경우가 많아 비장애인과 같은 정보를 받을 수 없는 것이 가장 큰 문제점이 된다.
    - 상품을 혼자 어렵게 찾아도 결제 과정에서 다른 사람 도움을 받게 된다.
- 문제 해결(기능과 기대효과)
    - 기능
        - 상품 조회 및 주문
        - 상품 관리
    - 필요 조건
        - 웹 서버, 데이터베이스, API를 활용해야 한다.
        - 이미지 분석을 위해 딥러닝 네트워크를 개발해야 한다.
        - 웹 접근성을 고려하여 웹 UI//UX를 연구해야 한다.
    - 기대효과
        - 시각장애인은 웹 쇼핑이 어려우며, 상품에 대한 정보를 알 수 없다. 이를 고려한 웹 접근성이 좋은 쇼핑몰이 만들어지면 웹 쇼핑을 하는 것에 부담이 덜할 것이다.

## ⚙️ 기술 스택

- 웹 페이지 구성
    - Front-end
        - HTML, CSS, JavaScript
    - Back-end
        - python, django
- Deep Learning
    - python virtualenv
    - CNN
    - Manhattan Distance(맨하탄 거리)

## **👫 팀 구성**

김호진, 성유정, 최하늘

## 💻 개발 내용

1. 웹 쇼핑몰 개발 순서
① Django 설치
② shop App 제작
③ Pillow를 활용한 image 사용환경 구축
④ cart App 제작
⑤ base html을 활용한 페이지 모듈화
⑥ Django administrator 사용
⑦ TTS 기능
⑧ 확대 축소 기능
2. 시스템 구조도
    <img width="444" alt="스크린샷 2022-12-01 오후 5 43 57" src="https://user-images.githubusercontent.com/67767912/205474211-f42e2d9f-e1a3-4d76-8f3a-834a2a9d22de.png">

    
3. 웹 서버 및 DB 연구
    
    <img width="545" alt="스크린샷 2022-12-01 오후 5 44 55" src="https://user-images.githubusercontent.com/67767912/205474214-6eea06f3-fc88-4304-86f1-ac03677734fa.png">

    - django administrator 사용
        - TTS 기능
        - 확대, 축소 기능
4. 딥러닝을 이용한 이미지 분석 연구
    1. 사용자가 상품 상세 페이지에서 이미지 분석을 요청
    2. 이미지 분석 서버에서 상품 사진에 대해 의복의 종류, 색상을 분석하고 결과를 웹에 전달
    - CNN 구조
    - Fashion-MNIST : 10가지 종류와 70,000개의 흑백 이미지로 구성된 의류에 대한 데이터셋
    - 파이썬을 이용한 색상 판단 : 색 분포 파악
        - Manhattan Distance(맨하탄 거리) : 두 점 사이의 거리를 구하는 방법이며, 거리가 가가울수록 유사도가 높다 - 색 분포 중 가장 비율이 높은 색상을 알아내고, 이 색상 값을 RGB 색상표와 비교하여 어떤 색상인지 판단
    
    <img width="301" alt="스크린샷 2022-12-01 오후 5 49 52" src="https://user-images.githubusercontent.com/67767912/205474221-9acd2adb-c2d9-4608-bcf5-34e7da25d5b1.png">

    1. 웹 쇼핑몰 UI/UX 구성
        <img width="557" alt="스크린샷 2022-12-01 오후 5 51 34" src="https://user-images.githubusercontent.com/67767912/205474224-d59d9ebe-bbc3-45bb-bc53-dcaf74882669.png">

        
        ```html
        <nav>
        	<a tabindex=“0”> 시각장애인 쇼핑몰 </a>
        	<div>
        		<ul>
        			<li>
        				<a tabindex=“0”> 카테고리 </a>
        				<a tabindex=“0”> 로그아웃 </a>
        				<a tabindex=“0”> 장바구니가 비었음 </a>
        			</li>
        		</ul>
        	</div>
        </nav>
        
        	<div>
        		<div>
        			<div>
        				<font tabindex=“0”> 당신을 위한 추천 상품 </font>
        				<div>
        					<div>
        						<div>
        							<font tabindex=“0”> 순위 </font>
        							<div>
        								<a tabindex=“-1”>
        									<img tabindex=“0”>
        								</a>
        							</div>
        							<div>
        								<span tabindex=“0”>상품</span>
        								<span tabindex=“0”>가격</span>
        							</div>
        						</div>
        					</div>
        					<!-- 나머지 두 이미지 부분 생략 -->
        				</div>
        			</div>
        		</div>
        	</div>
        ```
        

## **💻 내가 담당한 파트**

[웹 쇼핑몰 UI/UX 구성](https://www.notion.so/UI-UX-07397c28cec041b591ceb3aee8a0309d) 

## ✏️후기 및 에세이

선배님들의 작품을 역설계 하면서 딥러닝에 대해 더 이해할 수 있는 기회가 되었고, 웹 접근성이라는 개념에 대해 생각해 볼 수 있는 기회가 되었다.
