# Firewall  
## Intro  
	public zons의 설정파일  
	/etc/firewalld/zones/public.xml  
  
	방화벽 재로드
	#firewall-cmd --reload

## Port
	포트추가  
	#firewall-cmd --permanent --zone=public --add-port=포트  
	예) firewall-cmd --permanent --zone=public --add-port=80/tcp1  
	#firewall-cmd --reload  
  
	포트제거  
	#firewall-cmd --permanent --zone=public --remove-port=포트  
	예) firewall-cmd --permanent --zone=public --remove-port=80/tcp  
	#firewall-cmd --reload

## Service
	서비스추가  
	#firewall-cmd --permanent --zone=public --add-service=서비스  
	예) firewall-cmd --permanent --zone=public --add-service=http  
	#firewall-cmd --reload  
  
	서비스제거  
	#firewall-cmd --permanent --zone=public --remove-service=서비스  
	예) firewall-cmd --permanent --zone=public --remove-service=http  
	#firewall-cmd --reload  
## Command
	허용한포트 목록  
	#firewall-cmd --list-ports  
  
	방화벽상태 확인  
	#firewall-cmd --slate  
  
	활성화된 zone 목록  
	#firewall-cmd --get-active-zones  
  
	현재존재하는 서비스 목록  
	#firewall-cmd --get-service  
  
	public zone에 있는 서비스 목록  
	#firewall-cmd --zone+public --list-services
