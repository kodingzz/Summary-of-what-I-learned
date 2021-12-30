# 조건문과 반복문 

## 제어문  
조건문: 조건을 만족(참)할 때만 { } 수행(0-1번) //if문  
반복문: 조건을 만족하는 동안 { } 수행(0-n번)  // for,while문  

## 조건식의 예  
ex) str.equals("yes") : 문자열 str의 내용이 "yes"일때(대소문자 구분)  
ex) str.equalsIgnoreCase("yes") : 문자열 str의 내용이 "yes"일때 (대소문자 구분x)

## 괄호 {}
* 여러 문장 하나로 묶어주는 역할  
* 블럭안은 tab으로 들여쓰기하면 좋음  
* 블럭안의 문장이 하나일 경우  블럭 생략 가능  

if(조건식) {
  .
  .
  .
}

## 중첩 if문
if문안에 if, else문이 있으면 else문은 가장 가까운 if문과 연결된다.  

## switch문
처리해야하는 경우의 수가 많을 때 유용한 조건문  
if-else if문은 조건식이 여러개 나와야하는 반면 switch는 조건식이 1개만 나온다.  
if-else if문보다 간결하다.  
break를 만나면 switch문 종료  

## switch문의 제약조건
1. 조건식의 결과가 정수 또는 문자열이어야 한다.  
2. case문의 값은 정수,상수(문자포함), 문자열만 가능  
ex)  int num,result; final int ONE=1;  
switch(result){
  case '1':  
  case ONE:  
  case "Yes":  
  case num:    // error!!  변수x  
  case 1.0:     // error!!  실수x  

## 임의의 정수 만들기  Math.random()
Math.random()- 0.0-1.0 사이의 임의의 double값 반환  
0.0<=Math.random()<1.0  
ex) 1-3사이의 정수  
1. 각변에 3을 곱한다. 0.0<=Math.random()*3<3.0   범위: 0~2.9999999
2. 각 변을 int형으로 변환  0<=(int)(Math.random()*3)<3  범위: 0부터 2까지  
3. 각 변에 1을 더한다. 1<=(int)(Math.random()*3)+1<4  범위: 1부터 3까지  

## 반복문
for(초기화;조건식'증감식){...}  

**조건식,초기화,증감식 생략가능!**
for(;;){...}  


## while문 
반복횟수 모를 때  
while(조건식){
  //내용
}
## do-while문
do{
  //내용
}whle(조건식);  
do-while문은 최소한 1번이상 내용을 출력한다.  

## break문 
반복문을 벗어날때 사용  

## 이름붙은 반복문
반복문에 이름을 붙여서 하나 이상의 반복문을 벗어 날 수 있다.  
ex) break Loop1;


  
  
  
  
