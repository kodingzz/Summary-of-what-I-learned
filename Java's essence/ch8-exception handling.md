# 예외처리  
## 프로그램 오류  
컴파일러가 하는일 : 구문체크, 번역,최적화, 생략된 코드 추가  
컴파일 에러: 컴파일시에 발생하는 에러   - 실행자체가 안됨
런타임 에러: 실행시에 발생하는 에러    - 실행까진되지만 프로그램 종료
논리적 에러: 작성의도와 다르게 동작하는것  - 프로그램이 잘 동작하지만 내가 원하지 않는 답  

자바의 런타임 에러  
- 에러: 프로그램 코드에 의해 수습될 수 없는 심각한 오류  
- 예외: 수습될 수 있는 다소 미약한 오류  
- 에러는 어쩔수 없지만 예외는 처리할 수 있다.  

예외 처리
- 정의: 예외의 발생에 대비한 코드를 작성하는 것  
- 목적: 프로그램의 비정상 종료를 막기위해  

예외 클래스  
Exception  
- Exception 클래스와 그 자손들: 사용자의 실수와 같은 외적인 요인에 의해 발생하는 예외  
- RuntimeException클래스와 그 자손들: 프로그래머의 실수로 발생하는 예외  

예외 처리하기 try- catch문  
- 예외가 발생할 가능성이 있는 문장들을 try에 넣는다.  
- if문과 달리 try블럭이나 catch블러거 내에 포함된 문장이 하나뿐이어도 괄호 생략 x  
- 예외가 발생하면 이를 처리할 catch블럭을 찾아 내려간다.  
- 일치하는 catch블럭이없으면 예외는 처리안됨.  
- Exception이 선언된 catch블럭은 모든 예외를 처리하므로 마지막 catch블럭에 위치한다.  
- 
