# Emacs CheatSheet
## 커서이동

	Ctrl f, b, n, p (화살표와 동일)
	Ctrl v, Alt v (PgUp, PgDn)
	Ctrl a, Ctrl e (Home, End)
	Alt f, b (단어단위로 앞뒤이동)
	Alt a, e (문단 앞, 뒤로 이동)
	Alt <, > (파일의 처음, 끝으로 이동)
	Alt r (커서를 페이지의 처음,끝,가운데로 이동)
	Ctrl l (커서가 포함된 줄을 화면 처음, 끝, 가운데로 이동)
	Alt g - Alt g (원하는 줄로 이동)

## 삽입
	Ctrl o (빈줄 삽입, 커서 제자리)
	Ctrl j (빈줄 삽입, 커서 아래로)
	Ctrl x - i (파일 삽입)
	Ctrl y (kill한 내용 삽입)

## 삭제
	Ctrl d (커서에있는 글자삭제)
	BackSpace (커서 앞에있는 글자삭제)
	Alt d (커서에 있는 단어삭제)
	Alt BackSpace (커서 앞에있는 단어삭제)
	Ctrl k (커서부터 줄끝까지 삭제)
	Ctrl w (선택영역 kill)

## 영역
	Ctrl Space (영역선택시작, 종료)
	Ctrl x - Ctrl x (선택영역 시작지점 변경)
	Ctrl x - h (전체선택)
	Alt w (복사와 비슷)
	Ctrl w (잘라내기와 비슷)
	Ctrl y (붙여넣기와 비슷)

## 검색
	Ctrl s (아래로검색)
	Ctrl r (위로검색)
	Ctrl % (치환)
	Alt u (단어 대문자로 변경)
	Alt l (단어 소문자로 변경)
	Alt c (단어중 맨 앞글자만 대문자로변경)
	Ctrl x - Ctrl t (윗줄과 내용을 바꿈)
	Alt t (앞단어와 내용을 바꿈)
	Ctrl t (커서가 줄선두에 있을때 윗줄로 글자보냄)

## Dired 모드 (디렉토리 모드)
	f (파일 열기, 없으면 생성)
	v (파일 열기, 읽기전용)
	D (파일 삭제)
	g (디렉토리 목록갱신)
	R (파일 이름 변경)
	C (파일 복사)
	Alt x - make-directory - Enter (디렉토리 생성)
	+ (디렉토리 생성)

	Ctrl x - d (dired 모드 진입)
	Alt x - dired - Enter (dired 모드 진입)

## 인코딩
	Ctrl x - Enter - r (인코딩 보는방식 변경)
	Ctrl x - Enter - f (인코딩 저장방식 변경)
	(팁:미니버퍼에서 tab 누르면 목록 나옴)
	(euc-kr, cp949, utf-8, utf-16-le 등..)
	Ctrl \ (한글, 영어 변경)
	leftShift Space (한글, 영어 입력방식 변경)
	F9 (한글이나 자음등을 한자, 특수문자등으로 변환)

## 파일
	Ctrl x - Ctrl f (파일열기, 없을시 새로생성)
	Ctrl x - Ctrl s (파일 저장)
	Ctrl x - Ctrl w (다른이름으로 저장)
	Ctrl x - k (버퍼 닫기)
	Ctrl x - b (버퍼 이동, 화살표 위아래키로 목록열람가능)
	Ctrl x - Ctrl b (새 프레임을 열고 버퍼 목록 표시)

## 프레임(스프릿)
	Ctrl x - 2 (상하로 프레임분리)
	Ctrl x - 3 (좌우로 프레임분리)
	Ctrl x - 1 (현제프레임만 남기도 나머지 없애기)
	Ctrl x - 0 (현제프레임을 없애고 하나로 합치기)
	Ctrl x - ^ (현제프레임 수직크기 키우기, 보통 Ctrl - u 와 함께씀)
	Ctrl x - {, } (현제프레임 좌우크기 조절)
	Ctrl + (프레임들 크기 일정하게)
	Ctrl x - o (프레임간 이동)

## 기타
	Ctrl g (명령취소)
	Ctrl / (실행취소)
	Ctrl x - u (실행취소)
	Ctrl u - 숫자 (반복작업)
	Alt ! (간단한 쉘명령)
	Alt - shell - Enter (쉘 불러오기)
	Alt x - hexl-mode - Enter (헥사모드)
	Ctrl x - Enter - r - cp437 (nfo 파일볼때)
