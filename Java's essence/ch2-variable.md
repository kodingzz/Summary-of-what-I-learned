# Variable
## 변수란?
변수란 하나의 값을 저장할 수 있는 메모리 공간
## 변수의 선언
1. 변수 선언 이유: 값을 저장할 공간 마련하기 위해
2. 변수 선언 방법 : 변수타입 변수이름;  Ex) int age;
3. 변수에 값 저장하기 int age=25;  오른쪽의 값을 왼쪽에 저장
4. 변수는 클래스 변수, 인스턴스 변수, 지역변수 3가지  이중 지역변수는 꼭 초기화 먼저!  

* 5.변수의 값 읽어오기
    - 변수의 값이 필요한 곳에 변수의 이름적기 / int year=0,age=14; year=age+2000;
## 변수의 타입
>변수의 타입은 저장할 값의 타입에 따라 결정  
>저장할 값의 타입과 일치하는 타입으로 변수 선언 ex) char ch='가;
## 값의 타입
1. 문자-char
2. 숫자-정수-byte,short,int,long / 실수-float,double
3. 논리- boolean(True,False)

## 상수,리터럴
상수:한번만 값을 저장 가능한 변수  ex) final int MAX=100; //MAX는 상수
리터럴: 그 자체로 값을 의마하는 것 ex)100,200,'A'

# 리터럴의 접미사
정수형- 접미사 **L**(long)  ex)long lo=10000000000L;  
실수형- 접미사 **f,d**(float,double) ex)float f=1.4f;  / d는 생략가능

**char형은 문자한개만 받을 수 있다. string형은 여러문자를 받는다.**  
Ex)  
char ch='A'; / String str='abcdcd';  
byte b =127; /범위: -128~127
byte b= 128; / error  

# 리터럴의 접두사
int oct=0100;      /8진수로 표현  
int hex=0x100l;    /16진수로 표현  
int bin=0b0101;    /2진수로 표현  

# 변수와 리터럴의 타입 불일치
1. 범위가 변수>리터럴 인 경우 가능  
    - int i='A';  /문자 'A'의 문자코드 65가 i에 저장됨
    - long l=123; /long>int
    - double d=3.14f; / double >float
2. 범위가 변수<리터럴 인 경우 불가능
    - int i=3000000000; / int의 범위를 벗어남.
    - long l=3.14f; / long<float
3. byte,short 변수에 int 리터럴 저장가능
    - byte b=123;
# 문자와 문자열
String s ="A";
String s=" "; // 문자열은 빈 문자열 가능
char s=''; // error  문자는 빈 문자 불가능 

ex)  
"" + 7 -> "7" // 숫자 +빈 문자열 ->문자열(숫자)  
7+""+7 -> "7" +7 -> "7" +"7" -> "77"  

# 기본형 종류와 크기
 |종류/크기|1byte|2byte|4byte|8byte|
 |---|---|---|---|---|
 |논리형|boolean||||
 |문자형||char|||
 |정수형|byte|short|int|long|
 |실수형|||float|double|  
    
 정수형에서는 int, 실수형에서는 double이 많이 쓰임.  
    
 # 기본형 표현범위
 n비트로 표현할 수 있는 값의 개수: 2의 n승  
 n비트로 표현할 수 있는 부호없는 정수의 범위: 0 ~ 2의n승-1  
 n비트로 표현할 수 있는 부호있는 정수의 범위: -2의n-1승 ~ 2의n-1승-1  
    
 * 범위
    * byte(8비트):-2의7승~2의7승-1
    * short(16비트):-2의15승~2의15승-1
    * char(16비트):0~2의16승-1  //부호x
    * int(32비트): -2의31승~2의31승-1(~20억)
    * long(64비트): -2의 63승~2의63승-1(~800경)
    - float(32비트): 부호,지수,가수로 구성 // 가수부분은 정밀도와 관련이 있다. 10의7승<2의24승<10의8승 
    - double(64비트): 가수부분이 float의 2배이므로 정밀도도 float의 2배이다.  
    
 # 형식화된 출력 printf()
 > println()의 단점 -출력형식 지정불가
 >> 실수의 자릿수 조절불가  ex)소수점 n자리까지 출력..(x)
 >> 10진수로만 출력된다.   ex)println(0x1A) ->26  
    
 > printf()로 출력형식 지정가능
 >>printf("%.2f",10.0/3) // 3.33
 >>printf("%x",0x1A)  // 1A
    
# printf()의 지시자
> 정수를 10진수,8진수,16진수로 출력
>> printf("%d",15);  //15
>> printf("%o",15);  // 17
>> printf("%s", **Integer.toBinaryString(15)**); // 1111  
    
> 8진수와 16진수에 접두사 붙이기
>>printf("%#o",15);  // 017  
>>printf("%#x",15);  // 0xf  
    
> 실수 출력을 위한 지시자
>>%f- 지수형식(%e), 간략한 형식(%g)
>>> 실수 출력 ->%f
>>> 숫자에 0이 많이 들어갈때 ->%e  

> 정수
>> printf("[%5d]\n",10) // [   10]  
>> printf("[%-5d]\n",10) // [10   ]  
>> printf("[%05d]\n",10) // [00010] 
    
> 실수  
>> printnf("d=%14.10f\n",d) // 전체 14자리중에서 소수점아래 10자리, 정수 앞쪽은 공백 소수점아래는 0으로 채운다.
    
>문자열  
>> printf("[%s]\n",url)  //[wwww.~~]  
>> printf("[%.8s]\n",url)  //  [www.code]  전체문자중 8글자만 
    
# 화면에서 입력받기 -Scanner
> Scanner: 화면으로부터 데이터를 입력받는 기능을 제공하는 클래스
> Scanner를 사용
>> 1.import문 추가  // import java.util.Scanner;
>> 2. Scanner 객체 생성  // Scanner scanner = new Scanner(System.in);  
>> 3. Scanner 객체 이용 // int num= scanner.nextInt(); 입력받은 정수를 num에 저장  
    String input=scanner.nextLine(); //입력받은 내용을 input에 저장  
    int num= Integer.parseInt(input); // 문자열 input을 숫자 num으로 변환  

***숫자를 문자열로 바꾸는 방법: 숫자+" "
문자열을 숫자로 바꾸는 방법: Integer.parseInt(input)***

# 타입간의 변환방법  
1. 숫자를 문자로 변환 - 숫자에 '0'을 더한다.  
2. 문자를 숫자로 변환 - 문자에 '0'을 뺀다.  
3. 숫자를 문자열로 변환 - 숫자에 " "을 더한다.  
4. 문자열을 숫자로 변환 - Integer.parseInt("3")  
5. 문자를 문자열로 변환 - 문자에 " "을 더한다.  
6. 문자열을 문자로 변환 - "3".charAt(0) -> '3'
 
    
