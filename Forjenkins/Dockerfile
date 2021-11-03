FROM jenkins/jenkins:jdk11
# 해당 파일은 jenkins 이미지를 빌드하기 위한 Dockerfile임.

# 도커 실행을 위한 root 계정으로 전환
USER root

# 도커 설치
COPY docker_install.sh /docker_install.sh
# 도커 설치 쉘 스크립트 docker_install.sh
RUN chmod +x /docker_install.sh
RUN /docker_install.sh

# 설치 후 도커 그룹의 jenkins 계정 생성 후 해당 계정으로 변경
RUN groupadd -f docker
RUN usermod -aG docker jenkins
USER jenkins