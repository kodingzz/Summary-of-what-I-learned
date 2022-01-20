# 객체지향 언어
- 코드의 재사용성이 높고 유지보수 용이 ,중복 코드 제거  
- 객체지향 언어 = 프로그래밍 언어 + 객체지향개념(규칙)  

- 객체지향 프로그래밍(OOP)  
oop의 핵심 개념  
 1. 캡슐화  
 2. 상속  
 3. 추상화  
 4. 다형성  

## 클래스와 객체
 클래스: 객체를 정의해 놓은 것  
 클래스의 용도: 객체 생성하는데 사용  
ex)  
|클래스|객체|
|---|---|
|제품 설계도|제품|
|tv설계도|tv|  

**즉, tv는 객체이고, tv설계도는 클래스이다. ** 

- 객체 구성요소 - 속성(변수)과 기능(메서드)  
하드웨어를 소프트웨어로 변환(프로그램)해서 컴퓨터에서 사용 가능  
ex) TV(객체)  
속성- 크기,길이,높이...(변수)  
기능- 켜기,끄기,볼륨높이기...(메서드)  

- 객체==인스턴스  
인스턴스: 틀정 클래스로부터 생성된 객체 ex) tv인스턴스  
인스턴스화: 클래스로  인스턴스(객체)생성  

## 하나의 소스파일에 여러 클래스 작성
1. public class가 있는 경우 소스파일의 이름과 일치(대소문자 구분)해야 한다.  
2. public class가 없는경우 일치하지 않아도 된다.  
3. 하나의 소스파일에는 하나의 public class만 존재  

## 객체 생성과 사용  
1. 클래스 작성(설계도)  
2. 객체 생성  
  클래스 객체를 참조하기 위한 참조변수 선언  
  Tv t= new Tv();   // t는 tv를 조종하기 위한 리모콘같은 존재  , tv 객체 생성후 tv객체의 주소를 t에 저장   
  
|t|
|----|
|0x100|   
 
<Tv 객체>
|주소=0x100|
|---|
|color=null|
|power=false|
|channel=0|
|power()|
|channelUp()|
|channelDown()|  
  
3. 객체 사용  
t.channel=7; // tv 인스턴스의 변수 channel 값 지정   
t.channelDown();   // tv 메서드 호출  
tv클래스의 멤버(변수,메서드)모두 사용 가능하다.  


## 객체 배열
- 객체 배열 == 참조변수 배열  
- Tv tv1,tv2,tv3  -> Tv[] tvarr= new Tv[3];  // Tv 참조변수 3개  
- tvarr[0]=new Tv();
- tvarr[1]=new Tv();
- tvarr[2]=new Tv();   // 각각의 참조변수에 객체지정   
간단히 하면,  Tv[] tvarr= { new Tv(), new Tv(), new Tv() };   

참조변수 배열은 여러개의 참조변수를 하나의 배열로 묶은 것  

## 클래스 
클래스는 설계도 외에도 데이터+함수, 사용자 정의 타입으로도 정의된다. 
1. 데이터+ 함수  
변수: 하나의 데이터 저장공간  
배열: 같은종류의 여러 데이터 하나로 저장가능한 공간  
구조체: 여러데이터를 하나로 저장 가능한 공간  
클래스: 데이터(변수)와 함수(메서드)의 결합   

2. 사용자 정의 타입  
원하는 타입(클래스)을 직접 만들 수 있음.  
ex) class Time{
        int hour;
        int minute;
        int second;
        }
Time t= new Time();  
t.hour, t.minute등 값 지정  

## 변수의 종류
클래스 영역- instance variable(iv), class variable(cv)  
메서드 영역- local variable(lv)   // lv는 메서드 내에서만 유효  
cv는 iv앞에 static을 붙인 변수이다.  
객체는 iv를 묶어놓은 것.  따라서  객체생성 필수  
cv는 객체생성 필요x  

## 클래스 변수와 인스턴스 변수
Card c= new Card();  //객체 생성  
width, height이 cv라고 할때,  
c.width=200;  
c.height=300;  
Card.width=200;  
Card.height=300;   // cv앞에는 참조변수보다 클래스 이름을 쓴다.  

## 메서드(함수)
- 문장들을 묶어놓은것 { }  
- 메서드 생성후 메서드 호출  
- 하나의 메서드는 하나의 기능만 수행  

### 메서드= 선언부 + 구현부  
int add(int x,int y){   --> 선언부   // 입력 0-n개 가능
     int result =x + y;  
     return result;     --> 구현부    // 출력 0-1개 가능  
    }
 
### 메서드 호출  
ex) print99danAll();  
int result= add(3,5);  

## return문
메서드 종료하고 호출한곳으로 돌아가는 역할  

## 호출 스택
- 메서드가 호출되면 호출스택에 메모리가 할당된다.  
- 하나의 메서드가 실행중이면 나머지는 대기한다.  
- 메서드가 종료되면 스택에서 해제된다.  

## 기본형 매개변수
- 기본형 매개변수: 변수의 값을 읽기만 할 수 있다.(변경불가)  
- 참조형 매개변수: 변수의 값을 읽고 변경 할수있다.  

## 참조형 매개변수
참조변수(객체의 주소)를 이용해서 값을 읽고 쓰고 변경 할 수 있다.  

## static 메서드 인스턴스 메서드
메서드앞에 static 붙은것과 안붙은것의 차이  
### 인스턴스 메서드  
- 인스턴스 생성후, 참조변수.메서드이름()으로 호출  
- 인스턴스 멤버와 관련된 작업을 하는 메서드  
- 메서드 내에서 iv 사용 가능  

### static 메서드  
- 객체 생성없이 클래스이름.메서드이름()으로 호출  
- 인스턴스 멤버와 관련없는 작업을 하는 메서드  
- 메서드 내에서 iv사용 불가  

인스턴스 메서드는 iv가 사용되기 때문에 반드시 객체생성(iv묶음)을 해야하는 반면,  
static 메서드는 lv가 사용되기 때문에 객체 생성없이 사용 가능하다.  

**static 메서드는 인스턴스 메서드 호출 불가능(변수도 마찬가지)**  

## 오버로딩 : 한 클래스 안에 같은 이름의 메서드 여러개 정의 
자바에서는 오버로딩을 지원한다.  
오버로딩이 성립하기위한 조건  
1. 매서드 이름이 같아야한다.  
2. 매개변수의 갯수 또는 타입이 달라야한다.  
3. 반환 타입은 영향없다.  
메서드 이름이 같으면 같은 기능수행을 한다.  

## 생성자  
인스턴스가 생성될때마다 호출되는 인스턴스 초기화  
ex) Time t = new Time(12,34,56);  
생성자  
- 생성자이름은 클래스이름과 같아야한다.  
- 리턴값이 없다.  
- 모든 클래스는 반드시 생성자 가져야한다.  
Card c= new Card();   // 우항의 Card()는 생성자 호출

### 기본생성자
- 매개변수가 없는 생성자  
- 생성자가 하나도 없다면  컴파일러가 자동 추가   
- Point() {}  // 클래스이름() {}  

## 생성자 this()
- 생성자에서 다른 생성자 호출할때 사용  
- 다른 생성자 호출시 첫줄에서만 사용가능!  

## 참조변수 this
- 생성자 this()와 전혀 관계 없다.  
- 인스턴스 자신을 가리키는 참조변수  ex) this.color= color;  
- lv와 iv를 구별할때 사용  
- 생성자, 인스턴스 메서드에서만 사용가능  

## 변수 초기화  
- 지역변수는 수동 초기화해야함  
- 멤버변수(iv,cv)는 자동 초기화(0)된다.  

## 멤버변수 초기화  
- 클래스변수 초기화 시점: 클래스가 처음 로딩될때 한번  
- 인스턴스 변수: 인스턴스가 생성될때마다  
### 초기화 순서
cv->iv  
자동 초기화(0) -> 간단 초기화(=) -> 복잡 초기화( static 블럭,인스턴스 블럭, 생성자)  







