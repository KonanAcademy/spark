

# docker 환경 셋팅
* centos 7에 docker 설정 - https://docs.docker.com/installation/centos/
* selinux 문제 해결 -https://rbgeek.wordpress.com/2012/08/06/how-to-disable-selinux-on-centos-without-rebooting/

# spark-notebook docker image 셋 & 실행
* 이미지 풀링 
  - https://hub.docker.com/r/jupyter/all-spark-notebook/
  - docker pull jupyter/all-spark-notebook
* 컨테이너 실행 
  - https://github.com/jupyter/docker-stacks/tree/master/all-spark-notebook
  - docker run -d -p [외부포트]:[컨테이너노출포트] -e GRANT_SUDO=yes --name [컨테이너별명] jupyter/all-spark-notebook
    - docker run -d -p 8888:8888 -e GRANT_SUDO=yes --name run_spark_notebook jupyter/all-spark-notebook
  
