# nginx 시작하기

## 초기 설정 (centos)
- 저장소 추가
  - sudo vi /etc/yum.repos.d/nginx.repo
- 다음 내용 입력
  ~~~java
  [nginx]
  name = nginx repo
  baseurl = http://nginx.org/packages/centos/7/$basearch/
  gpgcheck = 0
  enabled = 1
  ~~~
- baseurl 찾기
  - nginx install toturial 참고
  - 표준버전: http://nginx.org/packages/centos/$releasever/$basearch/
  - 최신버전: http://nginx.org/packages/mainline/centos/$releasever/$basearch/
- nginx 설치
  - sudo yum install -y nginx
- nginx 시작
  - systemctl start nginx
  - systemctl enable nginx

## 초기 설정 (ubuntu)
- 설치: sudo apt-get install nginx
- 확인: nginx -v
- 설정파일 경로
  - /etc/nginx
  - /usr/local/nginx/conf, /usr/local/etc/nginx
  - sudo find / -name nginx.conf

## 주요 명령어
- 시작
  - sudo service nginx start
  - sudo systemctl start nginx
  - sudo /etc/init.d/nginx start
- 재시작
  - sudo service nginx restart
  - sudo systemctl restart nginx
  - sudo /etc/init.d/nginx restart
- 중지
  - sudo service nginx stop
  - sudo systemctl stop nginx
  - sudo /etc/init.d/nginx stop
- 상태
  - sudo service nginx status
  - sudo systemctl status nginx
- 설정 reload
  - sudo service nginx reload
  - sudo systemctl reload nginx
  - sudo nginx -s reload
- 설정파일 syntax 확인
  - sudo nginx -t

## 주요 설정
- nginx.conf
  - worker_processes (갯수);
  - 코어 갯수 그대로 또는 코어 갯수 n-1개
- server {}
  - listen 80; 기본 포트
  - server_name localhost; 접속 도메인, sub.domain.com 등
- location / {}
  - root html;
  - index index.html index.htm;
- location ~ /세부경로$ {}
  - proxy_pass 하위경로;
