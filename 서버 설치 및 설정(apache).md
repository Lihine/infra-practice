
# 웹서버 개요
 - 클라이언트 요청에 대해 서비스제공
 - HTTP프로토콜/포트번호 80번 사용
 - 클라이언트/서버 구조로 이루어짐

## 웹서버 프로그램
 - 다수의 클라이언트 요청에 대해 HTML문서 및 실행결과를 제공해주는 프로그램

## 일반 웹 서버 동작
 1. URL 입력
 1. IP주소로 변환(DNS서버)
 1. 해당 HTML페이지 요청
 1. 요청분석(HTML파일 읽기)
 1. HTML파일 전송
 1. HTML태그분석(웹브라우저)

## APM이란
 - Apache 웹 서버, PHP 프로그래밍언어, MySQL데이터베이스의 앞글자
 - 웹개발을 하는데 가장 많이 쓰이는 공개 솔류션

## Apache 웹 서버
 - NCSA HTTPD 기반
 - A PatCH server 라는 이름의 유래
 - 소스공개되어 있고 무료사용 가능
 - Unix, linux, Windows 모두 사용가능
 - 한글 및 다중언어 지원
 - 최대 255사용자 동시처리 가능

## Apache 설치방법
 1. 리눅스 설치 시 선택 설치
 1. 소스다운로드 & 컴파일(http://archive.apache.org/dist/httpd/httpd-2.0.6.3.tar.gz)
 1. ```./configure --prefix=/etc/httpd --enable-shared=max; make; make install```
 1. 패키지 관리자로 설치: 메뉴 → 시스템 관리  → Add/Remove software

## 웹 서비스 시작
 - 시스템 → 관리 → 서비스 → httpd를 Start

## 웹 서버 관련 디렉토리
 - /etc/httpd/conf/httpd.conf: 웹 서버 설정파일
 - /etc/rc.d/init.d/httpd: 서비스 실행/종료 스크립트
 - /var/www/cgi-bin/html/index.html: 홈페이지
 - /usr/sbin/apachectl: 데몬 등등..

## 아파치 웹서버 실행
 1. 터미널에서 실행: ```httpd -k start```
 1. 종료: ```httpd -k stop```
 1. 재시작: ```httpd -k restart```

## 웹서버 실행환경 설정
 - /etc/httpd/conf의 httpd.conf 파일

## 웹서버 동작확인
 - 웹브라우저 → URL창에 'http://localhost' 입력

## APM 설치
 - 설치 전 확인: ```rpm -qa | egrep "^(httpd|php|mysql)"```
 - 설치: ```yum install httpd mysql mysql-server php php-mysql```
 - 설치 후 확인: ```rpm -qa | egrep "^(httpd|php|mysql)" | sort -n```
 - 서비스 등록확인: ```service httpd status```, ```service mysqld status```, ```php -v```
