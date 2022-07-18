# 4주차 기업과제 : 아이디어콘서트 <br/>

## 프로젝트 진행 기간

`2022.07.18`
 <br/>


## 사용 기술

- Typescript, NestJS
- Github,  AWS EC2(ubuntu), NGINX, Elastic IP
 <br/>

## 서비스 개요


- AWS EC2를 사용해서 Nest.js 프로젝트 배포
<br/>

## 요구사항 분석


1. WAS : NGINX 사용 → Nginx Reverse-Proxy 설정

```jsx
server {
        listen 80;

        access_log /var/log/nginx/reverse-access.log;
        error_log /var/log/nginx/reverse-error.log;

        location / {
                    proxy_pass http://127.0.0.1:3000;
  }
}
```
<br/>

2. 탄력적 IP 사용 → [15.164.111.188] 주소사용
    

![스크린샷 2022-07-18 오후 2 12 08](https://user-images.githubusercontent.com/85995802/179450491-51e3a54a-745c-40c5-b03c-f2be7e29e157.png)
<br/>
 <br/>
3. Django 프로젝트 생성 → Nest.js 프로젝트 생성
<br/>
 <br/>
4. IP/api/hello 로 접속하였을때 웹브라우져 상에서 Hello 표시 → 15.165.111.188/api/hello 접속시 ‘Hello’ 표시

![스크린샷 2022-07-18 오후 2 09 27](https://user-images.githubusercontent.com/85995802/179450464-e55edb69-7b98-41eb-aa7f-51d5cbb6f6e7.png)
