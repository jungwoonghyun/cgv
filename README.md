# cgv

### 회원 정보
```

```

### 영화 + 가격

**movie file 안에는 Movie.java와 MovieMain.java가 있다.**

MovieMain.java에는 여러 함수들의 실행 절차가 설명되어있다.
Movie.java에는 MovieMain.java에 있는 여러 함수들이 들어 있다.


1. Movie.java

  **영화목록**
  + 함수 moviename() : 영화 목록에 따라 영화 이름을 출력
  + 함수 movie_choice() : 숫자를 수신해 예매한 영화 이름을 저장
  
  **좌석**
  - 함수 showseat() : 지정된 행과 열의 숫자만큼 좌석들을 보여준다. 
  - 함수 show_choosed_seat() : 입력받은 행(char 형태의 알파벳)과 입력받은 열(정수값)으로 선택된 좌석을 입력받아 선택된 좌석을 보여준다.
  
  **가격**
  -가격에 대한 공식은 다음과 같이 설정하였다.
  
  1.앞에 두줄은 11000원 다음 두줄은 12500원 마지막 두줄은 15000원으로 뒤로 갈수록 '기본 좌석 가격'이 오른다.
  2.구매 수단에 따라 할인률이 다르게 적용된다.
  3.구매자의 나이에 따라 할인률이 또 다르게 적용된다.
  4.2번과 3번의 할인률을 합쳐서 할인률을 만들고 '기본 좌석 가격' X '최종 할인률' = '최종가격' 이라는 공식을 만든다
  
  - 함수 cost() : 좌석에 따라 '기본 좌석 가격'을 결정해준다.
  - 함수 show_buyway() : 구매 수단들을 보여준다.
  - 함수 choose_buyway() : 구매 수단을 결정해준다.
  - 함수 buyDC() : 구매 수단에 따른 할인률 결정
  - 함수 AgeDC() : 나이 별 할인률 결정


2. MovieMain.java
  - 위의 Movie.java 속 함수들을 이용해 UI를 구성한다. 구성 순서는 다음과 같다.
  
  1. moviename()으로 예매가능 영화 표시
  2. 예매할 영화의 번호를 수신
  3. movie_choice()로 고른 영화 제목 저장
  
  4. showseat()로 고를 수 있는 좌석을 표시
  5. 원하는 좌석의 행과 열을 입력 (행은 int 타입으로 열은 char 타입으로 수신)
  6. 선택된 좌석만 다른좌석과 다르게 모양을 바꾸어 표시한다
  
  7. 구매방법을 표시해준다
  8. 구매방법을 입력받는다.
  9. 나이 입력을 요청한다.
  10. 나이를 입력받는다.
  11. 구매방법에 따른 할인률 + 나이에 따른 할인률을 총합으로 하여 전체 할인률을 계산한다.
  12. 선택한 좌석 행의 위치에 따라 '기본 좌석 가격'을 설정한다.
  13. 기본 좌석 가격*(1-할인률) = 최종가격  이라는 공식에 따라 최종 가격을 결정해준다.
  14. 예매한 영화, 기본 좌석 가격, 나이, 할인된 최종가격을 보여준다.