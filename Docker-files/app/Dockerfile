FROM openjdk:11 AS BUILD_IMAGE
#Tis is based on debian hence apt
RUN apt update && apt install maven -y
#clone the source code from your repostory
RUN git clone https://github.com/Abbeydauda20/vprofile_project.git
#cd into the branch and install git and container
RUN cd vprofile_project && git checkout container && mvn install



FROM tomcat:9-jre11
RUN rm -rf /user/loca;/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile_project/target/vprofile-v2.war /user/local/tomcat/webapps/RC

EXPOSE 8080
CMD ["catalin.sh", "run"]