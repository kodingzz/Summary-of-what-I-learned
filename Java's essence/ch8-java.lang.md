#java.lang패키지와 클래스  

## Object클래스
- 모든 클래스의 최고조상. 오직 11개의 메서드만을 가지고있다.  
-  clone,equals,hashcode,toString..등등  

### (boolean) equals()  
- 객체 자신과 주어진 객체를 비교한다.  
- Object클래스의 equals()는 객체의 주소를 비교  
- equals(Object obj) 오버라이딩: iv값을 비교하기위해 equls()를 오버라이딩해야함.  
- 원래 object의 equals()는 주소비교를하지만 오버라이딩하여 iv값을 비교한다.  

## hashcode()  
- 객체의 해시코드를 반환하는 메서드  
- 객체의 주소를 int로 변환해서 반환  
- equals()를 오버라이딩하면 hashcode()도 오버라이딩 해야한다.  
- euqals()결과가 true이면 두 객체의 해시코드는 같아야하기 때문이다.  
- 객체마다 다른 해시코드값이 필요할 때는 System.identityHashCode(Object obj) 이용  

## toString()  
- 객체를 문자열로 변환하기위한 메서드  
- 객체를 문자열로 바꾼다는것은 iv값들을 문자열로 바꾼다는것과 같은의미이다.  
- 따라서 toString()을 오버라이딩할때 iv값들을 이용하여 출력하는것이다.  

## String클래스  
- 문자열을 다루기위한 클래스  
- 내용을 변경할수 없는 클래스  
- 덧셈 연잔자를 이용한 문자열 결합은 성능이 떨어진다.  
- 문자열 결합이나 변경이 잦으면, 내용변경이 가능한 StringBuffer사용한다.  

## 문자열 비교
- String str="abc" // 하나의 문자열을 여러 참조변수가 가리킨다.  
- String str1=new String("abc") 
- String str=2new String("abc") // 항상 새로운 문자열이 만들어진다.  

## 문자열 리터럴  
- 문자열 리터럴은 프로그램 실해애시 자동으로 생성된다.  
## 빈 문자열  
- 내용이 없는 문자열. 크기가 0인 char형 배열을 저장하는 문자열  
- String str="";  // 빈 문자열로 초기화  

## join()과 StringJoiner  
- join()은 여러문자열 사이에 구분자를 넣어서 결합한다.  

## StringBuffer 클래스
- 문자열을 저장하고 다루기위한 클래스  
- String과 달리 내용을 변경할 수 있다.  

## StringBuffer의 생성자  
- 배열은 길이 변경불가. 공간이 부족하면 새로운 배열 생성해야한다.  
- 1. 새 배열생성  2. 내용복사 3. 참조변경  
- 저장할 문자열의 길이 고려해서 적절한 크기로 생성해야한다.  

## StringBuffer의 비교  
- StringBuffer는 equals()가 오버라이딩되어있지 않다.(주소비교)  
- String으로 변환후에 equals()로 비교해야한다.  
