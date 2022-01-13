# 날짜와 시간 & 형식화  

## 날짜와 시간
- java.util.Date :날짜와 시간을 다룰 목적으로 만들어진 클래스  
- java.util.Calendar(Date를 개선한 클래스 단점존재)-> java.Time패키지 추가  

## Calendar클래스  
- 추상클래스이므로 getInstance()를 통해 구현된 객체를 얻어야한다.  
- Calendar cal =Calendar.getInstance();  
- get()으로 날짜와 시간필드 가져오기 : int get(int field)  
- set()으로 날짜와 시간 지정할수 있다.  
- clear()는 Calendar객체의 모든 필드를 초기화  
- add()는 특정필드의 값을 증가또는 감소(다른 필드에 영향o)
- roll()은 특정필드의 값을 증가또는 감소(다른 필드에 영향x)- YEAR,MONYH,DATE같은 필드에 영향 X  

## Date와 Calendar간의 변환  
- Calendar를 Date로 변환 
- Calendar cal=Calendar.getInstance();  / Date d= new Date(cal.getTimeInMillis());  
- Date를 Calendar로 변환  
- Date d = new Date(); / Calendar cal= Calendar.getInstance() / cal.setTime(d);

## 형식화 클래스
- DecimalFormat  
- 숫자를 형식화할 때 사용(숫자-> 형식문자열)   .format()
- 특정형식의 문자열을 숫자로 변환할때도 사용(형식문자열->숫자)  .parse()
- SimpleDateFormat()  
- 날짜와 시간을 다양한 형식으로 출력할 수 있게 해준다.  
- 문자열에서 날찌와 시간을 뽑아 낼 수도 있다.  
- 
