# 🌐 Connect to Your AWS EC2 Instance

   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-172-31-11-187 ~]$ sudo su -
[root@ip-172-31-11-187 ~]# yum install docker -y
Amazon Linux 2023 Kernel Livepatch repository                                                                                                                                                                             318 kB/s |  29 kB     00:00    
Dependencies resolved.
==========================================================================================================================================================================================================================================================
 Package                                                            Architecture                                       Version                                                              Repository                                               Size
==========================================================================================================================================================================================================================================================
Installing:
 docker                                                             x86_64                                             25.0.13-1.amzn2023.0.2                                               amazonlinux                                              46 M
Installing dependencies:
 container-selinux                                                  noarch                                             4:2.242.0-1.amzn2023                                                 amazonlinux                                              58 k
 containerd                                                         x86_64                                             2.1.4-1.amzn2023.0.2                                                 amazonlinux                                              23 M
 iptables-libs                                                      x86_64                                             1.8.8-3.amzn2023.0.2                                                 amazonlinux                                             401 k
 iptables-nft                                                       x86_64                                             1.8.8-3.amzn2023.0.2                                                 amazonlinux                                             183 k
 libcgroup                                                          x86_64                                             3.0-1.amzn2023.0.1                                                   amazonlinux                                              75 k
 libnetfilter_conntrack                                             x86_64                                             1.0.8-2.amzn2023.0.2                                                 amazonlinux                                              58 k
 libnfnetlink                                                       x86_64                                             1.0.1-19.amzn2023.0.2                                                amazonlinux                                              30 k
 libnftnl                                                           x86_64                                             1.2.2-2.amzn2023.0.2                                                 amazonlinux                                              84 k
 pigz                                                               x86_64                                             2.5-1.amzn2023.0.3                                                   amazonlinux                                              83 k
 runc                                                               x86_64                                             1.3.3-2.amzn2023.0.1                                                 amazonlinux                                             3.9 M

Transaction Summary
==========================================================================================================================================================================================================================================================
Install  11 Packages

Total download size: 74 M
Installed size: 280 M
Downloading Packages:
(1/11): container-selinux-2.242.0-1.amzn2023.noarch.rpm                                                                                                                                                                   2.1 MB/s |  58 kB     00:00    
(2/11): iptables-libs-1.8.8-3.amzn2023.0.2.x86_64.rpm                                                                                                                                                                      16 MB/s | 401 kB     00:00    
(3/11): iptables-nft-1.8.8-3.amzn2023.0.2.x86_64.rpm                                                                                                                                                                      6.4 MB/s | 183 kB     00:00    
(4/11): libcgroup-3.0-1.amzn2023.0.1.x86_64.rpm                                                                                                                                                                           3.5 MB/s |  75 kB     00:00    
(5/11): libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64.rpm                                                                                                                                                            2.3 MB/s |  58 kB     00:00    
(6/11): libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64.rpm                                                                                                                                                                     1.5 MB/s |  30 kB     00:00    
(7/11): libnftnl-1.2.2-2.amzn2023.0.2.x86_64.rpm                                                                                                                                                                          3.0 MB/s |  84 kB     00:00    
(8/11): pigz-2.5-1.amzn2023.0.3.x86_64.rpm                                                                                                                                                                                2.7 MB/s |  83 kB     00:00    
(9/11): runc-1.3.3-2.amzn2023.0.1.x86_64.rpm                                                                                                                                                                               72 MB/s | 3.9 MB     00:00    
(10/11): containerd-2.1.4-1.amzn2023.0.2.x86_64.rpm                                                                                                                                                                        76 MB/s |  23 MB     00:00    
(11/11): docker-25.0.13-1.amzn2023.0.2.x86_64.rpm                                                                                                                                                                          78 MB/s |  46 MB     00:00    
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                                                                                                     120 MB/s |  74 MB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                                                                                                                                  1/1 
  Installing       : runc-1.3.3-2.amzn2023.0.1.x86_64                                                                                                                                                                                                1/11 
  Installing       : containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                                                                                                                          2/11 
  Running scriptlet: containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                                                                                                                          2/11 
  Installing       : pigz-2.5-1.amzn2023.0.3.x86_64                                                                                                                                                                                                  3/11 
  Installing       : libnftnl-1.2.2-2.amzn2023.0.2.x86_64                                                                                                                                                                                            4/11 
  Installing       : libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64                                                                                                                                                                                       5/11 
  Installing       : libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64                                                                                                                                                                              6/11 
  Installing       : iptables-libs-1.8.8-3.amzn2023.0.2.x86_64                                                                                                                                                                                       7/11 
  Installing       : iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                                                                                                                                        8/11 
  Running scriptlet: iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                                                                                                                                        8/11 
  Installing       : libcgroup-3.0-1.amzn2023.0.1.x86_64                                                                                                                                                                                             9/11 
  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                                                                                                                                  10/11 
  Installing       : container-selinux-4:2.242.0-1.amzn2023.noarch                                                                                                                                                                                  10/11 
  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                                                                                                                                  10/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                                                                                                                           11/11 
  Installing       : docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                                                                                                                           11/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                                                                                                                           11/11 
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /usr/lib/systemd/system/docker.socket.

  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                                                                                                                                  11/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                                                                                                                           11/11 
  Verifying        : container-selinux-4:2.242.0-1.amzn2023.noarch                                                                                                                                                                                   1/11 
  Verifying        : containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                                                                                                                          2/11 
  Verifying        : docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                                                                                                                            3/11 
  Verifying        : iptables-libs-1.8.8-3.amzn2023.0.2.x86_64                                                                                                                                                                                       4/11 
  Verifying        : iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                                                                                                                                        5/11 
  Verifying        : libcgroup-3.0-1.amzn2023.0.1.x86_64                                                                                                                                                                                             6/11 
  Verifying        : libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64                                                                                                                                                                              7/11 
  Verifying        : libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64                                                                                                                                                                                       8/11 
  Verifying        : libnftnl-1.2.2-2.amzn2023.0.2.x86_64                                                                                                                                                                                            9/11 
  Verifying        : pigz-2.5-1.amzn2023.0.3.x86_64                                                                                                                                                                                                 10/11 
  Verifying        : runc-1.3.3-2.amzn2023.0.1.x86_64                                                                                                                                                                                               11/11 

Installed:
  container-selinux-4:2.242.0-1.amzn2023.noarch      containerd-2.1.4-1.amzn2023.0.2.x86_64                  docker-25.0.13-1.amzn2023.0.2.x86_64           iptables-libs-1.8.8-3.amzn2023.0.2.x86_64      iptables-nft-1.8.8-3.amzn2023.0.2.x86_64     
  libcgroup-3.0-1.amzn2023.0.1.x86_64                libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64      libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64      libnftnl-1.2.2-2.amzn2023.0.2.x86_64           pigz-2.5-1.amzn2023.0.3.x86_64               
  runc-1.3.3-2.amzn2023.0.1.x86_64                  

Complete!
[root@ip-172-31-11-187 ~]# systemctl start docker
[root@ip-172-31-11-187 ~]# systemctl status docker
● docker.service - Docker Application Container Engine
     Loaded: loaded (/usr/lib/systemd/system/docker.service; disabled; preset: disabled)
     Active: active (running) since Wed 2025-12-03 11:02:24 UTC; 9s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
    Process: 27911 ExecStartPre=/bin/mkdir -p /run/docker (code=exited, status=0/SUCCESS)
    Process: 27912 ExecStartPre=/usr/libexec/docker/docker-setup-runtimes.sh (code=exited, status=0/SUCCESS)
   Main PID: 27913 (dockerd)
      Tasks: 9
     Memory: 30.1M
        CPU: 208ms
     CGroup: /system.slice/docker.service
             └─27913 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock --default-ulimit nofile=32768:65536

Dec 03 11:02:23 ip-172-31-11-187.ec2.internal systemd[1]: Starting docker.service - Docker Application Container Engine...
Dec 03 11:02:23 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:23.617403817Z" level=info msg="Starting up"
Dec 03 11:02:23 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:23.649675947Z" level=info msg="Loading containers: start."
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.019059522Z" level=info msg="Loading containers: done."
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.030818985Z" level=info msg="Docker daemon" commit=165516e containerd-snapshotter=false storage-driver=overlay2 version=25.0.13
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.030980622Z" level=info msg="Daemon has completed initialization"
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.057483792Z" level=info msg="API listen on /run/docker.sock"
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal systemd[1]: Started docker.service - Docker Application Container Engine.
[root@ip-172-31-11-187 ~]# yum install git -y
Last metadata expiration check: 0:03:01 ago on Wed Dec  3 11:01:42 2025.
Dependencies resolved.
==========================================================================================================================================================================================================================================================
 Package                                                       Architecture                                        Version                                                                 Repository                                                Size
==========================================================================================================================================================================================================================================================
Installing:
 git                                                           x86_64                                              2.50.1-1.amzn2023.0.1                                                   amazonlinux                                               53 k
Installing dependencies:
 git-core                                                      x86_64                                              2.50.1-1.amzn2023.0.1                                                   amazonlinux                                              4.9 M
 git-core-doc                                                  noarch                                              2.50.1-1.amzn2023.0.1                                                   amazonlinux                                              2.8 M
 perl-Error                                                    noarch                                              1:0.17029-5.amzn2023.0.2                                                amazonlinux                                               41 k
 perl-File-Find                                                noarch                                              1.37-477.amzn2023.0.7                                                   amazonlinux                                               25 k
 perl-Git                                                      noarch                                              2.50.1-1.amzn2023.0.1                                                   amazonlinux                                               41 k
 perl-TermReadKey                                              x86_64                                              2.38-9.amzn2023.0.2                                                     amazonlinux                                               36 k
 perl-lib                                                      x86_64                                              0.65-477.amzn2023.0.7                                                   amazonlinux                                               15 k

Transaction Summary
==========================================================================================================================================================================================================================================================
Install  8 Packages

Total download size: 7.9 M
Installed size: 41 M
Downloading Packages:
(1/8): git-2.50.1-1.amzn2023.0.1.x86_64.rpm                                                                                                                                                                               1.6 MB/s |  53 kB     00:00    
(2/8): git-core-doc-2.50.1-1.amzn2023.0.1.noarch.rpm                                                                                                                                                                       56 MB/s | 2.8 MB     00:00    
(3/8): perl-Error-0.17029-5.amzn2023.0.2.noarch.rpm                                                                                                                                                                       1.9 MB/s |  41 kB     00:00    
(4/8): git-core-2.50.1-1.amzn2023.0.1.x86_64.rpm                                                                                                                                                                           63 MB/s | 4.9 MB     00:00    
(5/8): perl-File-Find-1.37-477.amzn2023.0.7.noarch.rpm                                                                                                                                                                    893 kB/s |  25 kB     00:00    
(6/8): perl-Git-2.50.1-1.amzn2023.0.1.noarch.rpm                                                                                                                                                                          1.4 MB/s |  41 kB     00:00    
(7/8): perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64.rpm                                                                                                                                                                    1.6 MB/s |  36 kB     00:00    
(8/8): perl-lib-0.65-477.amzn2023.0.7.x86_64.rpm                                                                                                                                                                          721 kB/s |  15 kB     00:00    
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                                                                                                      60 MB/s | 7.9 MB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                                                                                                                                  1/1 
  Installing       : git-core-2.50.1-1.amzn2023.0.1.x86_64                                                                                                                                                                                            1/8 
  Installing       : git-core-doc-2.50.1-1.amzn2023.0.1.noarch                                                                                                                                                                                        2/8 
  Installing       : perl-lib-0.65-477.amzn2023.0.7.x86_64                                                                                                                                                                                            3/8 
  Installing       : perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64                                                                                                                                                                                      4/8 
  Installing       : perl-File-Find-1.37-477.amzn2023.0.7.noarch                                                                                                                                                                                      5/8 
  Installing       : perl-Error-1:0.17029-5.amzn2023.0.2.noarch                                                                                                                                                                                       6/8 
  Installing       : perl-Git-2.50.1-1.amzn2023.0.1.noarch                                                                                                                                                                                            7/8 
  Installing       : git-2.50.1-1.amzn2023.0.1.x86_64                                                                                                                                                                                                 8/8 
  Running scriptlet: git-2.50.1-1.amzn2023.0.1.x86_64                                                                                                                                                                                                 8/8 
  Verifying        : git-2.50.1-1.amzn2023.0.1.x86_64                                                                                                                                                                                                 1/8 
  Verifying        : git-core-2.50.1-1.amzn2023.0.1.x86_64                                                                                                                                                                                            2/8 
  Verifying        : git-core-doc-2.50.1-1.amzn2023.0.1.noarch                                                                                                                                                                                        3/8 
  Verifying        : perl-Error-1:0.17029-5.amzn2023.0.2.noarch                                                                                                                                                                                       4/8 
  Verifying        : perl-File-Find-1.37-477.amzn2023.0.7.noarch                                                                                                                                                                                      5/8 
  Verifying        : perl-Git-2.50.1-1.amzn2023.0.1.noarch                                                                                                                                                                                            6/8 
  Verifying        : perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64                                                                                                                                                                                      7/8 
  Verifying        : perl-lib-0.65-477.amzn2023.0.7.x86_64                                                                                                                                                                                            8/8 

Installed:
  git-2.50.1-1.amzn2023.0.1.x86_64             git-core-2.50.1-1.amzn2023.0.1.x86_64              git-core-doc-2.50.1-1.amzn2023.0.1.noarch        perl-Error-1:0.17029-5.amzn2023.0.2.noarch        perl-File-Find-1.37-477.amzn2023.0.7.noarch       
  perl-Git-2.50.1-1.amzn2023.0.1.noarch        perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64        perl-lib-0.65-477.amzn2023.0.7.x86_64           

Complete!
[root@ip-172-31-11-187 ~]# git clone https://github.com/chintu-cloud/Docker_Python_Flask-Project.git
Cloning into 'docker_python_flask-project'...
remote: Enumerating objects: 91, done.
remote: Counting objects: 100% (91/91), done.
remote: Compressing objects: 100% (59/59), done.
Receiving objects: 100% (91/91), 26.87 KiB | 26.87 MiB/s, done.
remote: Total 91 (delta 46), reused 56 (delta 26), pack-reused 0 (from 0)
Resolving deltas: 100% (46/46), done.
[root@ip-172-31-11-187 ~]# ls
docker_python_flask-project
[root@ip-172-31-11-187 ~]# cd docker_python_flask-project
[root@ip-172-31-11-187 docker_python_flask-project]# ls
Dockerfile  README.md  app.py  deploy+process_ec2_process  nginx-process  requirements.txt
[root@ip-172-31-11-187 docker_python_flask-project]# docker build -t simple-flask-app:latest .
[+] Building 13.9s (9/9) FINISHED                                                                                                                                                                                                          docker:default
 => [internal] load build definition from Dockerfile                                                                                                                                                                                                 0.0s
 => => transferring dockerfile: 296B                                                                                                                                                                                                                 0.0s
 => [internal] load metadata for docker.io/library/python:3.6                                                                                                                                                                                        0.2s
 => [internal] load .dockerignore                                                                                                                                                                                                                    0.0s
 => => transferring context: 2B                                                                                                                                                                                                                      0.0s
 => [internal] load build context                                                                                                                                                                                                                    0.0s
 => => transferring context: 81.10kB                                                                                                                                                                                                                 0.0s
 => [1/4] FROM docker.io/library/python:3.6@sha256:f8652afaf88c25f0d22354d547d892591067aa4026a7fa9a6819df9f300af6fc                                                                                                                                  9.0s
 => => resolve docker.io/library/python:3.6@sha256:f8652afaf88c25f0d22354d547d892591067aa4026a7fa9a6819df9f300af6fc                                                                                                                                  0.0s
 => => sha256:f8652afaf88c25f0d22354d547d892591067aa4026a7fa9a6819df9f300af6fc 1.86kB / 1.86kB                                                                                                                                                       0.0s
 => => sha256:d097a4907a8ec079df5ac31872359c2de510f82214c0448e926393b376d3b60d 2.22kB / 2.22kB                                                                                                                                                       0.0s
 => => sha256:0e29546d541cdbd309281d21a73a9d1db78665c1b95b74f32b009e0b77a6e1e3 54.92MB / 54.92MB                                                                                                                                                     0.6s
 => => sha256:9b829c73b52b92b97d5c07a54fb0f3e921995a296c714b53a32ae67d19231fcd 5.15MB / 5.15MB                                                                                                                                                       0.1s
 => => sha256:cb5b7ae361722f070eca53f35823ed21baa85d61d5d95cd5a95ab53d740cdd56 10.87MB / 10.87MB                                                                                                                                                     0.2s
 => => sha256:54260638d07c5e3ad24c6e21fc889abbc8486a27634c0892086ff71f3f44b104 9.27kB / 9.27kB                                                                                                                                                       0.0s
 => => sha256:6494e4811622b31c027ccac322ca463937fd805f569a93e6f15c01aade718793 54.57MB / 54.57MB                                                                                                                                                     0.7s
 => => sha256:6f9f74896dfa93fe0172f594faba85e0b4e8a0481a0fefd9112efc7e4d3c78f7 196.51MB / 196.51MB                                                                                                                                                   2.6s
 => => extracting sha256:0e29546d541cdbd309281d21a73a9d1db78665c1b95b74f32b009e0b77a6e1e3                                                                                                                                                            1.4s
 => => sha256:5e3b1213efc56598e78bd602983945c164de2a37205e06a62dada823124dc743 6.29MB / 6.29MB                                                                                                                                                       0.8s
 => => sha256:404f02044bac0432ca522cbb9f254b1c91fcea6806bfeef0be0b243b2f31bab7 235B / 235B                                                                                                                                                           0.8s
 => => sha256:9fddfdc56334f2e6efad7e241bf5e7459c40ed105c5478676f41c1244bd96752 14.21MB / 14.21MB                                                                                                                                                     0.9s
 => => sha256:c4f42be2be53b900ebffc040c1df13de538434ccc5f5d954a56848a6169a3a3f 2.21MB / 2.21MB                                                                                                                                                       0.9s
 => => extracting sha256:9b829c73b52b92b97d5c07a54fb0f3e921995a296c714b53a32ae67d19231fcd                                                                                                                                                            0.1s
 => => extracting sha256:cb5b7ae361722f070eca53f35823ed21baa85d61d5d95cd5a95ab53d740cdd56                                                                                                                                                            0.1s
 => => extracting sha256:6494e4811622b31c027ccac322ca463937fd805f569a93e6f15c01aade718793                                                                                                                                                            1.3s
 => => extracting sha256:6f9f74896dfa93fe0172f594faba85e0b4e8a0481a0fefd9112efc7e4d3c78f7                                                                                                                                                            3.9s
 => => extracting sha256:5e3b1213efc56598e78bd602983945c164de2a37205e06a62dada823124dc743                                                                                                                                                            0.2s
 => => extracting sha256:9fddfdc56334f2e6efad7e241bf5e7459c40ed105c5478676f41c1244bd96752                                                                                                                                                            0.3s
 => => extracting sha256:404f02044bac0432ca522cbb9f254b1c91fcea6806bfeef0be0b243b2f31bab7                                                                                                                                                            0.0s
 => => extracting sha256:c4f42be2be53b900ebffc040c1df13de538434ccc5f5d954a56848a6169a3a3f                                                                                                                                                            0.1s
 => [2/4] COPY . /app                                                                                                                                                                                                                                2.1s
 => [3/4] WORKDIR /app                                                                                                                                                                                                                               0.0s
 => [4/4] RUN pip install -r requirements.txt                                                                                                                                                                                                        2.4s
 => exporting to image                                                                                                                                                                                                                               0.1s 
 => => exporting layers                                                                                                                                                                                                                              0.1s 
 => => writing image sha256:5ac94cb2e4c051a6ad1a6b5c99a0a39375cf8ff2f8641f8bf8938ddd843b20fc                                                                                                                                                         0.0s 
 => => naming to docker.io/library/simple-flask-app:latest 
[root@ip-172-31-11-187 docker_python_flask-project]# docker run -d -p 5000:5000 simple-flask-app                                                                                                                                                          
11fb0e9e65a7709fa89c02e728741365166b9b564da7dd0ca2083e0f91e831f4                                                                                                                                                                                          
[root@ip-172-31-11-187 docker_python_flask-project]# docker ps
CONTAINER ID   IMAGE              COMMAND           CREATED          STATUS          PORTS                                       NAMES
11fb0e9e65a7   simple-flask-app   "python app.py"   21 seconds ago   Up 21 seconds   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   adoring_mcclintock
[root@ip-172-31-11-187 docker_python_flask-project]# git clone https://github.com/CloudTechDevOps/swiggy-nodejs-devops-project.git
Cloning into 'swiggy-nodejs-devops-project'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (32/32), done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 92 (delta 21), reused 7 (delta 7), pack-reused 60 (from 2)
Receiving objects: 100% (92/92), 1.80 MiB | 68.15 MiB/s, done.
Resolving deltas: 100% (25/25), done.
[root@ip-172-31-11-187 docker_python_flask-project]# ls
Dockerfile  README.md  app.py  deploy+process_ec2_process  docker  nginx-process  requirements.txt





# 🚀 Docker Python Flask Project

This repository contains a simple **Flask application** packaged with **Docker** for easy deployment.

---

## ✅ What’s in the repo
- `app.py` → Flask application entrypoint  
- `requirements.txt` → Python dependencies  
- `Dockerfile` → Docker build instructions  
- `README.md` → Setup and deployment guide  

---

## 📦 Deployment Steps

1. **Clone the repository**  
   ```bash
   git clone https://github.com/CloudTechDevOps/docker_python_flask-project.git && cd docker_python_flask-project
   ```

2. **Inspect or update dependencies**  
   Open `requirements.txt` to confirm required packages; add new ones if needed and update the file.

3. **Build the Docker image**  
   ```bash
   docker build -t simple-flask-app:latest .
   ```

4. **Run the Docker container**  
   ```bash
   docker run -d -p 5000:5000 simple-flask-app
   ```

5. **Access the application**  
   Visit `http://localhost:5000` (or `http://<server-ip>:5000` if remote).

6. **Verify the response**  
   Use browser or `curl http://localhost:5000/` to confirm output from `app.py`.

---

## 🛠️ Production Readiness (Optional)

- The built-in Flask server is not recommended for production.  
- Use **Gunicorn** (or uWSGI) as WSGI server, optionally behind **Nginx**.  
- Example production Dockerfile:

  ```dockerfile
  FROM python:3.9-slim
  WORKDIR /app
  COPY requirements.txt .
  RUN pip install -r requirements.txt
  COPY . .
  CMD ["gunicorn", "--bind", "0.0.0.0:5000", "app:app"]
  ```

---

## 🚀 Deploying on Server / Cloud (Optional)

- Push image to Docker Hub or private registry.  
- Pull and run image on server.  
- Use **Docker Compose** if multiple services are needed.  
- Hosting platforms (e.g., Koyeb) allow direct Docker image deployment.

---

## 📂 Example docker-compose.yml (Optional)

```yaml
version: "3.8"
services:
  web:
    build: .
    container_name: flask_app
    ports:
      - "5000:5000"
    command: gunicorn --bind 0.0.0.0:5000 app:app
```

---

## 🔗 References
- [GitHub Repo](https://github.com/CloudTechDevOps/docker_python_flask-project.git)  
- [Dockerize Flask App - GeeksforGeeks](https://www.geeksforgeeks.org/dockerize-your-flask-app/?utm_source=chatgpt.com)  
- [Deploy Flask Apps with Docker - Codezup](https://codezup.com/deploy-flask-apps-with-docker-step-by-step-guide/?utm_source=chatgpt.com)  
- [Flask Deployment on Koyeb](https://www.koyeb.com/tutorials/python-flask-application-deployment-on-koyeb?utm_source=chatgpt.com)  

---

---

This README is **ready-to-use**: every step is in one line, no missing instructions, and optional production/cloud deployment notes are included.  

Would you like me to also prepare a **production-ready Dockerfile + docker-compose.yml combo** so you can copy-paste directly without editing?
