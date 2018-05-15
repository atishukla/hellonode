# Hello Node
TODO:

Jenkins fail with 

docker: error while loading shared libraries: libltdl.so.7: cannot open shared object file: No such file or directory
[Pipeline] }

Investigate

Docker ran with 

docker run -p 8080:8080 -v /var/run/docker/sock:/var/run/docker.sock -v /var/jenkins_home:/var/jenkins_home -v$(which docker):/usr/bin/docker --name myjenkins jenkins/jenkins:lts

Check after removing docker.sock the error as client will then be mapped
