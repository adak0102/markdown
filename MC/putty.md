login as: lab05
Authenticating with public key "imported-openssh-key"
[lab05@ip-172-31-42-102 ~]$ date
Sat Nov  7 16:52:26 KST 2020
[lab05@ip-172-31-42-102 ~]$ ls
[lab05@ip-172-31-42-102 ~]$ ll
total 0
[lab05@ip-172-31-42-102 ~]$ ls
[lab05@ip-172-31-42-102 ~]$ ll
total 0
[lab05@ip-172-31-42-102 ~]$ cat > test.txt
Have an mice day

[lab05@ip-172-31-42-102 ~]$ mkdir mydir
[lab05@ip-172-31-42-102 ~]$ ls
mydir  test.txt
[lab05@ip-172-31-42-102 ~]$ ll
total 4
drwxr-xr-x. 2 lab05 multi  6 Nov  7 17:17 mydir
-rw-r--r--. 1 lab05 multi 18 Nov  7 17:17 test.txt
[lab05@ip-172-31-42-102 ~]$ pwd
/home/lab05
[lab05@ip-172-31-42-102 ~]$ cd mydir
[lab05@ip-172-31-42-102 mydir]$ pwd
/home/lab05/mydir
[lab05@ip-172-31-42-102 mydir]$ cd ..
[lab05@ip-172-31-42-102 ~]$ cd ..
[lab05@ip-172-31-42-102 home]$ pwd
/home
[lab05@ip-172-31-42-102 home]$ cd ..
[lab05@ip-172-31-42-102 /]$ pwd
/
[lab05@ip-172-31-42-102 /]$ ls
bin   dev        etc   lib    media  opt   root  sbin  sys   tmp  var
boot  downloads  home  lib64  mnt    proc  run   srv   temp  usr
[lab05@ip-172-31-42-102 /]$ who
lab06    pts/0        2020-11-07 16:37 (116.35.102.57)
lab04    pts/1        2020-11-07 16:33 (175.198.101.179)
lab05    pts/2        2020-11-07 16:48 (114.204.9.114)
[lab05@ip-172-31-42-102 /]$ mkdir test
mkdir: cannot create directory ‘test’: Permission denied
[lab05@ip-172-31-42-102 /]$ cd
[lab05@ip-172-31-42-102 ~]$ pwd
/home/lab05
[lab05@ip-172-31-42-102 ~]$ mkdir backup
[lab05@ip-172-31-42-102 ~]$ ls
backup  mydir  test.txt
[lab05@ip-172-31-42-102 ~]$ ls -a
.  ..  backup  .bash_logout  .bash_profile  .bashrc  mydir  .ssh  test.txt
[lab05@ip-172-31-42-102 ~]$ cd backup
[lab05@ip-172-31-42-102 backup]$ ls
emp.csv
[lab05@ip-172-31-42-102 backup]$ cat emp.csv
empno,ename,job,mgr,hiredate,sal,comm,deptno
7369,SMITH,CLERK,7902,1980-12-17,800,,20
7499,ALLEN,SALESMAN,7698,1981-02-20,1600,300,30
7521,WARD,SALESMAN,7698,1981-02-03,1250,500,30
7566,JONES,MANAGER,7839,1981-03-02,2975,,20
7654,MARTIN,SALESMAN,7698,1981-10-22,1250,1400,30
7698,BLAKE,MANAGER,7839,1981-05-01,2850,,30
7782,CLARK,MANAGER,7839,1981-09-06,2450,,10
7788,SCOTT,ANALYST,7566,1982-12-08,3000,,20
7839,KING,PRESIDENT,,1981-11-17,5000,,10
7844,TURNER,SALESMAN,7698,1984-10-08,1500,,30
7876,ADAMS,CLERK,7788,1983-01-12,1100,,20
7900,JAMES,CLERK,7698,1981-12-03,950,,30
7902,FORD,ANALYST,7566,1981-12-13,3000,,20
7934,MILLER,CLERK,7782,1982-01-25,1300,,10[lab05@ip-172-31-42-102 backup]$ cd
[lab05@ip-172-31-42-102 ~]$ mv backup data
[lab05@ip-172-31-42-102 ~]$ ls
data  mydir  test.txt
[lab05@ip-172-31-42-102 ~]$ ls data
emp.csv
[lab05@ip-172-31-42-102 ~]$ ls
data  mydir  test.txt
[lab05@ip-172-31-42-102 ~]$ ls
data  mydir  test.txt
[lab05@ip-172-31-42-102 ~]$ ls data
emp.csv               name-customers.csv     score.csv           stock valuation
greeting.txt          naverhotel1.txt        score_header.csv    survey.csv
hotel.txt             naverhotel.txt         score_noheader.csv  train.csv
iris.csv              picher_stats_2017.csv  score.xlsx          tweet_temp.csv
korean_stopwords.txt  product_click.log      seoul_geo.json
mpgdata.csv           product_click_new.log  stock-data.csv
mydata.json           read_csv_sample.csv    stock price.xlsx
[lab05@ip-172-31-42-102 ~]$