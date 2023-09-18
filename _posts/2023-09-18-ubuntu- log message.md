---
layout: post
title: 우분투 리눅스 에러 로그와 접근로그 실시간 보는 방법
content:  
실시간 접근 :sudo tail -f /var/log/apache2/access.log
실시간 에러 로그 보기:sudo tail -f /var/log/apache2/error.log


그외는 cat으로 해서 접근해서 봐도 된다.
 tail: 로그 파일의 끝 부분을 출력하는 명령입니다.
-f: 파일을 열어 실시간으로 변경 사항을 추적하는 옵션입니다.
sudo tail -f를 사용하면 로그 파일의 내용을 실시간으로 모니터링할 수 있습니다. 
이것은 주로 로그 파일을 감시하고 문제를 실시간으로 파악하거나, 디버깅 및 모니터링 목적으로 사용됩니다.


리눅스 시스템에서는 다양한 로그 파일이 있으며, 각 로그 파일은 시스템 및 애플리케이션의 다양한 활동을 기록합니다. 일반적으로 /var/log 디렉토리에 위치하며, 중요한 로그 파일 몇 가지를 아래에 나열합니다. 로그 파일은 시스템의 구성에 따라 다를 수 있으므로 실제로 존재하는 파일 및 경로가 다를 수 있습니다.

syslog: 시스템 로깅 메시지를 기록합니다. /var/log/syslog 또는 /var/log/messages로 저장될 수 있습니다.

auth.log: 사용자 로그인 및 인증에 관련된 정보를 포함합니다. /var/log/auth.log로 저장됩니다.

kern.log: 커널과 관련된 로그 메시지를 기록합니다. /var/log/kern.log로 저장됩니다.

dmesg: 부팅 중 커널 메시지를 확인할 수 있는 로그입니다. dmesg 명령으로 확인할 수 있습니다.

cron: 크론 작업에 관련된 정보를 기록합니다. /var/log/cron 또는 /var/log/cron.log로 저장될 수 있습니다.

mail.log: 메일 서버 (예: Postfix 또는 Sendmail)에서 발생한 메일 관련 로그를 기록합니다. /var/log/mail.log 또는 /var/log/maillog로 저장될 수 있습니다.

boot.log: 부팅 과정의 로그를 기록합니다. /var/log/boot.log로 저장됩니다.

apache2 또는 nginx: 웹 서버 로그는 웹 서버의 종류에 따라 다를 수 있으며, 주로 /var/log/apache2 또는 /var/log/nginx 디렉토리에 저장됩니다.

mysql 또는 postgresql: 데이터베이스 서버 로그는 데이터베이스 종류에 따라 다를 수 있으며, 주로 /var/log/mysql 또는 /var/log/postgresql 디렉토리에 저장됩니다.

secure: 시스템 보안 로그를 기록하며, /var/log/secure로 저장될 수 있습니다.

wtmp 또는 utmp: 사용자 로그인 기록을 저장합니다. /var/log/wtmp 또는 /var/run/utmp 등에 위치할 수 있습니다.

fail2ban.log: 보안 도구인 Fail2ban의 로그를 기록합니다. /var/log/fail2ban.log로 저장됩니다.


syslog 확인하기:      sudo cat /var/log/syslog
auth.log 확인하기:   sudo cat /var/log/auth.log
kern.log 확인하기:   sudo cat /var/log/kern.log
dmesg 확인하기:   dmesg
cron 확인하기:   sudo cat /var/log/cron.log
mail.log 확인하기:   sudo cat /var/log/mail.log
boot.log 확인하기:   sudo cat /var/log/boot.log
Apache 웹 서버 액세스 로그 확인하기:   sudo cat /var/log/apache2/access.log
Nginx 웹 서버 액세스 로그 확인하기:   sudo cat /var/log/nginx/access.log
MySQL 로그 확인하기 (예시 - MySQL 사용자에 따라 다름):   sudo cat /var/log/mysql/error.log
PostgreSQL 로그 확인하기 (예시 - PostgreSQL 사용자에 따라 다름):   sudo cat /var/log/postgresql/postgresql-<version>-main.log
secure 확인하기:   sudo cat /var/log/secure
wtmp 확인하기:   last
fail2ban.log 확인하기:   sudo cat /var/log/fail2ban.log

categories: develop
--------