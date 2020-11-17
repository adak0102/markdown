# MC aws server 

리눅스: 6대 , 멀티유저 운영체재 , 우리는 6대

팀당 한대씩 할당됨

각각 머신 조원끼리 나눠 씀

팀별 리눅스 머신 하나씩, 머신안에 적용되는 아이디

접속때 사용하는 계정 : shpark-big password:big1234(비밀번호 수정한거 기억 중요) region:seoul

쁘띠로 할떄는 계정이 또 다름:lab05

jupyternotebook port번호 : 8894

 jupyter lab --ip=0.0.0.0 --no-browser --port=8894

하나의 포트번호는 하나의 (머신에서) 사용가능함

서버 ip주소  : 3.35.110.29

aws  : 저녁10시 이후&일요일 운영안함 

-  https://multicampus-4th.signin.aws.amazon.com/console 

몽고 디비 여기에 넣어놓을 거임

머신이 기동 되어야 (instance기동 시키고 나서) 몽고DB에 접근할 수 있음;컴터 키듯이

aws에 들어오는거는 인스턴스 기동하고 먹통되면 재부팅할려고 들어옴

- putty

  브라우저같은 역할

  다른 머신에 들어가서 그 머신을 사용할 수 있게끔 해주는 애

  그럴려면 다른 머신의 ip주소를 알아야함 (우리  aws ip 주소)



- ls / ll(더 자세히)
- ctrl D : putty 명령어 다음 으로 하는 거
- pwd:print working directory
- 다른 디렉토리에서는 아무것도 못함. mkdir은 내 홈디렉토리 (자기한테 부여된 디렉토리)안에서만 작업을 할 수 있도록 제한 됨
- 관리자 계정 root는 어디서든 할 수 있긴함 
- 그냥 cd
- 하면 다시 내 홈디렉토리로 돌아오게 됨
- rm은 안쓰는게 좋음(복구 못함)
- cat > 파일만드는기능
- cat 파일내용 보는 기능 
- 쁘띠:들어가서 사용용도
- 파일 전송용도, 홈디렉토리에 올리기, 리눅스 파일 내려오기는 FZ사용 
- 리눅스에 있는 파일 내리고 올릴떄 FZ사용 
- ls -a : all모두 보임 .까지 (히든파일까지_중요한 파일들)
- mv backup data : backup 디렉토리 data로 이름 바꿈(디렉토리도 파일과 같음)
- ls data (디렉토리명)하면 그 디렉토리의 파일리스트가 뜸
- ls rm -rf backup  (r:directory f:무조건 지움 )  

---

자바스크립트.파이썬.스칼라.줄리아 정도는 아는게 좋음

분석전문가가 될거면



## FZ

host로그인 위에 맨 왼쪽 AWS로 접속