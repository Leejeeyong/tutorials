서비스 상태
$ service status

서비스 멈춤
$ systemctl stop sshd.service

서비스시작
$ systemctl start sshd.service

서비스 사용가능
$ systemctl enable sshd.service

윈도우의 ip보는

$ ifconfig

. 접속

      – ssh 사용자아이디@접속서버주소

      – $ ssh iwoo@192.168.1.100

2. 접속 종료

    – 명령어 : exit

    – 명령어 실행 결과 : Connection to 접속서버주소 closed.
