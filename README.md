# Technical_interview_2

기술면접 대비를 위한 IT 기초 정리 2탄 입니다.

# ➂ 웹 프로그래밍

#### <b>3.1 인터넷이란?</b>

![image](https://user-images.githubusercontent.com/93306939/170177180-d83fac26-d632-4863-87dc-e33994861dba.png)

**인터넷**  
 - 네트워크와 네트워크의 집합체
 - 전 세계의 네트워크를 하나로 묶어 놓은 것
 ( INTERconnected NETwork )
 
**인터넷의 탄생**  
 - 1969년 미국 국방부산하 연구기관인 ARPA의 연구용 네트워크인 ARPANET에서 유래
 - 인터넷이라는 용어는 1982년 TCP/IP 프로토콜이 개발 되면서 처음 사용 됨

------

#### <b>3.2 웹(Web)의 구조</b>

![image](https://user-images.githubusercontent.com/93306939/170805903-835cb8c3-1bc2-4799-a3ee-cd7cd85f31b1.png)

[URL 형식] - 프로토콜 IP : 포트 번호

------

#### <b>GET 방식과 POST 방식에 대해 설명하세요.</b>

![image](https://user-images.githubusercontent.com/93306939/170805968-98065ac1-2506-4bd4-a975-08b823c2f316.png)

**GET방식**

GET방식의 특징으로는 대표적으로 URL에 Parameter를 붙여서 전송한다는 것입니다.

```
ex) http://khj93.tistory.com/test_api?param1=value1&param2=value2
```

URL뒤에  ?  를 사용하여 Parameter를 작성하게 되고  &  을 붙여 여러개의 Parameter를 구분하게 됩니다.
이런식으로 GET방식은 데이터를 전송하게 되며 URL에 Parameter를 전송하기 때문에 body영역을 사용하지 않는다.
또한 URL에 데이터를 실어 보내기 때문에 대용량 데이터 전송을 하기에 제한 사항이 있다.
한번 요청시 URL포함 255자 까지 전송이 가능하며 HTTP/1.1 에서는 2048자 까지 가능합니다.

**POST방식**

POST 방식의 특징으로는 대표적으로 GET 방식과는 달리 body영역에 데이터를 실어 보낸다는 점입니다. Body에 데이터를 실어 보내기 때문에 데이터 전송양에 길이 제한이 없으며 대용량 데이터를 보내는데 적합합니다.

또한 POST로 데이터를 전송할때에는 Body영역 데이터 타입을 Header Content-Type에 명시를 해줘야 합니다. POST방식은 GET방식과는 달리 보내는 데이터를 URL를 통해 볼 수 없어 보안적으로 안전하다곤 하지만 다른 툴을 사용하여 POST영역의 데이터를 확인이 가능하기 때문에 안심해서는 안됩니다.

```
ex)
HEADER 영역  

Content-Type:application/json; charset=UTF-8

.....

BODY 영역

{
	"param1":"value1",
	"param2":"value2"
}
```
------
