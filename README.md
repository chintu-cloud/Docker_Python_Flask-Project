


# 🚀 Docker Python Flask Project

This repository contains a simple **Flask application** packaged with **Docker** for easy deployment.


Here’s a clean **file structure layout** for your `docker_python_flask-project` repo. I’ve styled it so it looks polished and easy to scan 👇  


# 📂 Project File Structure

```
docker_python_flask-project/
├── app.py                # Main Flask application entrypoint
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker build instructions
├── docker-compose.yml    # (Optional) Compose file for multi-service setup
├── README.md             # Documentation and deployment guide
└── __pycache__/          # Auto-generated Python cache files (ignored in .gitignore)
```

---

## 📝 Notes
- **app.py** → Contains your Flask routes and logic.  
- **requirements.txt** → Lists all Python packages needed (`Flask`, `gunicorn`, etc.).  
- **Dockerfile** → Defines how to build the container image.  
- **docker-compose.yml** → Useful if you add DB, cache, or multiple services.  
- **README.md** → Deployment instructions (already prepared).  
- **__pycache__/** → Generated automatically by Python, not needed in version control.  






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
# 🌐 Connect to Your AWS EC2 Instance
  ```
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
Amazon Linux 2023 Kernel Livepatch repository                                                                       318 kB/s |  29 kB     00:00    
Dependencies resolved.
=================================================================================================================================================
 Package                                 Architecture                   Version                            Repository                      Size
=================================================================================================================================================
Installing:
 docker                                   x86_64                  25.0.13-1.amzn2023.0.2                   amazonlinux                     46 M
Installing dependencies:
 container-selinux                        noarch                  4:2.242.0-1.amzn2023                     amazonlinux                     58 k
 containerd                               x86_64                  2.1.4-1.amzn2023.0.2                     amazonlinux                     23 M
 iptables-libs                            x86_64                  1.8.8-3.amzn2023.0.2                     amazonlinux                    401 k
 iptables-nft                             x86_64                  1.8.8-3.amzn2023.0.2                     amazonlinux                    183 k
 libcgroup                                x86_64                  3.0-1.amzn2023.0.1                       amazonlinux                     75 k
 libnetfilter_conntrack                   x86_64                  1.0.8-2.amzn2023.0.2                     amazonlinux                     58 k
 libnfnetlink                             x86_64                  1.0.1-19.amzn2023.0.2                    amazonlinux                     30 k
 libnftnl                                 x86_64                  1.2.2-2.amzn2023.0.2                     amazonlinux                     84 k
 pigz                                     x86_64                  2.5-1.amzn2023.0.3                       amazonlinux                     83 k
 runc                                     x86_64                  1.3.3-2.amzn2023.0.1                     amazonlinux                    3.9 M

Transaction Summary
===================================================================================================================================================
Install  11 Packages

Total download size: 74 M
Installed size: 280 M
Downloading Packages:
(1/11): container-selinux-2.242.0-1.amzn2023.noarch.rpm                                                              2.1 MB/s |  58 kB     00:00    
(2/11): iptables-libs-1.8.8-3.amzn2023.0.2.x86_64.rpm                                                                 16 MB/s | 401 kB     00:00    
(3/11): iptables-nft-1.8.8-3.amzn2023.0.2.x86_64.rpm                                                                 6.4 MB/s | 183 kB     00:00    
(4/11): libcgroup-3.0-1.amzn2023.0.1.x86_64.rpm                                                                      3.5 MB/s |  75 kB     00:00    
(5/11): libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64.rpm                                                       2.3 MB/s |  58 kB     00:00    
(6/11): libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64.rpm                                                                1.5 MB/s |  30 kB     00:00    
(7/11): libnftnl-1.2.2-2.amzn2023.0.2.x86_64.rpm                                                                     3.0 MB/s |  84 kB     00:00    
(8/11): pigz-2.5-1.amzn2023.0.3.x86_64.rpm                                                                           2.7 MB/s |  83 kB     00:00    
(9/11): runc-1.3.3-2.amzn2023.0.1.x86_64.rpm                                                                          72 MB/s | 3.9 MB     00:00    
(10/11): containerd-2.1.4-1.amzn2023.0.2.x86_64.rpm                                                                   76 MB/s |  23 MB     00:00    
(11/11): docker-25.0.13-1.amzn2023.0.2.x86_64.rpm                                                                     78 MB/s |  46 MB     00:00    
----------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                120 MB/s |  74 MB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                        1/1 
  Installing       : runc-1.3.3-2.amzn2023.0.1.x86_64                                                                                      1/11 
  Installing       : containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                2/11 
  Running scriptlet: containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                2/11 
  Installing       : pigz-2.5-1.amzn2023.0.3.x86_64                                                                                        3/11 
  Installing       : libnftnl-1.2.2-2.amzn2023.0.2.x86_64                                                                                  4/11 
  Installing       : libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64                                                                             5/11 
  Installing       : libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64                                                                    6/11 
  Installing       : iptables-libs-1.8.8-3.amzn2023.0.2.x86_64                                                                             7/11 
  Installing       : iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                              8/11 
  Running scriptlet: iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                              8/11 
  Installing       : libcgroup-3.0-1.amzn2023.0.1.x86_64                                                                                   9/11 
  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                        10/11 
  Installing       : container-selinux-4:2.242.0-1.amzn2023.noarch                                                                        10/11 
  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                        10/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                 11/11 
  Installing       : docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                 11/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                 11/11 
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /usr/lib/systemd/system/docker.socket.

  Running scriptlet: container-selinux-4:2.242.0-1.amzn2023.noarch                                                                        11/11 
  Running scriptlet: docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                 11/11 
  Verifying        : container-selinux-4:2.242.0-1.amzn2023.noarch                                                                         1/11 
  Verifying        : containerd-2.1.4-1.amzn2023.0.2.x86_64                                                                                2/11 
  Verifying        : docker-25.0.13-1.amzn2023.0.2.x86_64                                                                                  3/11 
  Verifying        : iptables-libs-1.8.8-3.amzn2023.0.2.x86_64                                                                             4/11 
  Verifying        : iptables-nft-1.8.8-3.amzn2023.0.2.x86_64                                                                              5/11 
  Verifying        : libcgroup-3.0-1.amzn2023.0.1.x86_64                                                                                   6/11 
  Verifying        : libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64                                                                    7/11 
  Verifying        : libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64                                                                             8/11 
  Verifying        : libnftnl-1.2.2-2.amzn2023.0.2.x86_64                                                                                  9/11 
  Verifying        : pigz-2.5-1.amzn2023.0.3.x86_64                                                                                       10/11 
  Verifying        : runc-1.3.3-2.amzn2023.0.1.x86_64                                                                                     11/11 

Installed:
  container-selinux-4:2.242.0-1.amzn2023.noarch      containerd-2.1.4-1.amzn2023.0.2.x86_64                  docker-25.0.13-1.amzn2023.0.2.x86_64              
  libcgroup-3.0-1.amzn2023.0.1.x86_64                libnetfilter_conntrack-1.0.8-2.amzn2023.0.2.x86_64      libnfnetlink-1.0.1-19.amzn2023.0.2.x86_64 
  runc-1.3.3-2.amzn2023.0.1.x86_64  

                                 iptables-libs-1.8.8-3.amzn2023.0.2.x86_64      iptables-nft-1.8.8-3.amzn2023.0.2.x86_64 
                                 libnftnl-1.2.2-2.amzn2023.0.2.x86_64           pigz-2.5-1.amzn2023.0.3.x86_64        
                  

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
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.030818985Z" level=info msg="Docker daemon" commit=165516e containerd-
snapshotter=false storage-driver=overlay2 version=25.0.13
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.030980622Z" level=info msg="Daemon has completed initialization"
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal dockerd[27913]: time="2025-12-03T11:02:24.057483792Z" level=info msg="API listen on /run/docker.sock"
Dec 03 11:02:24 ip-172-31-11-187.ec2.internal systemd[1]: Started docker.service - Docker Application Container Engine.
[root@ip-172-31-11-187 ~]# yum install git -y
Last metadata expiration check: 0:03:01 ago on Wed Dec  3 11:01:42 2025.
Dependencies resolved.
==================================================================================================================================================
 Package                          Architecture                   Version                           Repository                    Size
==================================================================================================================================================
Installing:
 git                               x86_64                 2.50.1-1.amzn2023.0.1                   amazonlinux                     53 k
Installing dependencies:
 git-core                          x86_64                 2.50.1-1.amzn2023.0.1                   amazonlinux                    4.9 M
 git-core-doc                      noarch                 2.50.1-1.amzn2023.0.1                   amazonlinux                    2.8 M
 perl-Error                        noarch                 1:0.17029-5.amzn2023.0.2                amazonlinux                     41 k
 perl-File-Find                    noarch                 1.37-477.amzn2023.0.7                   amazonlinux                     25 k
 perl-Git                          noarch                 2.50.1-1.amzn2023.0.1                   amazonlinux                     41 k
 perl-TermReadKey                  x86_64                 2.38-9.amzn2023.0.2                     amazonlinux                     36 k
 perl-lib                          x86_64                 0.65-477.amzn2023.0.7                   amazonlinux                     15 k

Transaction Summary
==================================================================================================================================================
Install  8 Packages

Total download size: 7.9 M
Installed size: 41 M
Downloading Packages:
(1/8): git-2.50.1-1.amzn2023.0.1.x86_64.rpm                                                                          1.6 MB/s |  53 kB     00:00    
(2/8): git-core-doc-2.50.1-1.amzn2023.0.1.noarch.rpm                                                                  56 MB/s | 2.8 MB     00:00    
(3/8): perl-Error-0.17029-5.amzn2023.0.2.noarch.rpm                                                                  1.9 MB/s |  41 kB     00:00    
(4/8): git-core-2.50.1-1.amzn2023.0.1.x86_64.rpm                                                                      63 MB/s | 4.9 MB     00:00    
(5/8): perl-File-Find-1.37-477.amzn2023.0.7.noarch.rpm                                                               893 kB/s |  25 kB     00:00    
(6/8): perl-Git-2.50.1-1.amzn2023.0.1.noarch.rpm                                                                     1.4 MB/s |  41 kB     00:00    
(7/8): perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64.rpm                                                               1.6 MB/s |  36 kB     00:00    
(8/8): perl-lib-0.65-477.amzn2023.0.7.x86_64.rpm                                                                     721 kB/s |  15 kB     00:00    
-----------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                 60 MB/s | 7.9 MB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                         1/1 
  Installing       : git-core-2.50.1-1.amzn2023.0.1.x86_64                                                                                   1/8 
  Installing       : git-core-doc-2.50.1-1.amzn2023.0.1.noarch                                                                               2/8 
  Installing       : perl-lib-0.65-477.amzn2023.0.7.x86_64                                                                                   3/8 
  Installing       : perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64                                                                             4/8 
  Installing       : perl-File-Find-1.37-477.amzn2023.0.7.noarch                                                                             5/8 
  Installing       : perl-Error-1:0.17029-5.amzn2023.0.2.noarch                                                                              6/8 
  Installing       : perl-Git-2.50.1-1.amzn2023.0.1.noarch                                                                                   7/8 
  Installing       : git-2.50.1-1.amzn2023.0.1.x86_64                                                                                        8/8 
  Running scriptlet: git-2.50.1-1.amzn2023.0.1.x86_64                                                                                        8/8 
  Verifying        : git-2.50.1-1.amzn2023.0.1.x86_64                                                                                        1/8 
  Verifying        : git-core-2.50.1-1.amzn2023.0.1.x86_64                                                                                   2/8 
  Verifying        : git-core-doc-2.50.1-1.amzn2023.0.1.noarch                                                                               3/8 
  Verifying        : perl-Error-1:0.17029-5.amzn2023.0.2.noarch                                                                              4/8 
  Verifying        : perl-File-Find-1.37-477.amzn2023.0.7.noarch                                                                             5/8 
  Verifying        : perl-Git-2.50.1-1.amzn2023.0.1.noarch                                                                                   6/8 
  Verifying        : perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64                                                                             7/8 
  Verifying        : perl-lib-0.65-477.amzn2023.0.7.x86_64                                                                                   8/8 

Installed:
  git-2.50.1-1.amzn2023.0.1.x86_64             git-core-2.50.1-1.amzn2023.0.1.x86_64              git-core-doc-2.50.1-1.amzn2023.0.1.noarch             
  perl-Git-2.50.1-1.amzn2023.0.1.noarch        perl-TermReadKey-2.38-9.amzn2023.0.2.x86_64        perl-lib-0.65-477.amzn2023.0.7.x86_64  

                    perl-Error-1:0.17029-5.amzn2023.0.2.noarch        perl-File-Find-1.37-477.amzn2023.0.7.noarch           
Complete!
[root@ip-172-31-11-187 ~]# git clone https://github.com/chintu-cloud/swiggy-nodejs-devops-project.git
Cloning into 'swiggy-nodejs-devops-project'...
remote: Enumerating objects: 92, done.
remote: Counting objects: 100% (32/32), done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 92 (delta 21), reused 7 (delta 7), pack-reused 60 (from 2)
Receiving objects: 100% (92/92), 1.80 MiB | 76.67 MiB/s, done.
Resolving deltas: 100% (25/25), done.
[root@ip-172-31-11-187 ~]# ls
docker_python_flask-project  swiggy-nodejs-devops-project
[root@ip-172-31-11-187 ~]# cd ^C
[root@ip-172-31-11-187 ~]# cd swiggy-nodejs-devops-project
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]# ls
Dockerfile  Kubernetes  Photos  README.md  package-lock.json  package.json  public  src
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]# vi dockerfile
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]# docker build -t swiggy-nodejs-app .
[+] Building 26.0s (11/11) FINISHED                                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                                               0.0s
 => => transferring dockerfile: 1.16kB                                                                                                             0.0s
 => [internal] load metadata for docker.io/library/node:16-slim                                                                                    0.2s
 => [internal] load .dockerignore                                                                                                                  0.0s
 => => transferring context: 2B                                                                                                                    0.0s
 => [1/6] FROM docker.io/library/node:16-slim@sha256:3ebf2875c188d22939c6ab080cfb1a4a6248cc86bae600ea8e2326aa03acdb8f                              2.3s
 => => resolve docker.io/library/node:16-slim@sha256:3ebf2875c188d22939c6ab080cfb1a4a6248cc86bae600ea8e2326aa03acdb8f                              0.0s
 => => sha256:ecdd21ad91a4e69294555b3e56a71a7382a58a9c54b02d9038bcd3821ba3d072 4.18kB / 4.18kB                                                     0.1s
 => => sha256:72f5a0bbd6d5f85fce35070bd624cf69c2ceb91424afe8a5ed2a02442cdd711c 35.25MB / 35.25MB                                                   0.6s
 => => sha256:6d65359ecb29ff24f2322d5ad308f0a8a95980706ae2e76315a267474402aa3a 2.73MB / 2.73MB                                                     0.2s
 => => sha256:3ebf2875c188d22939c6ab080cfb1a4a6248cc86bae600ea8e2326aa03acdb8f 776B / 776B                                                         0.0s
 => => sha256:549225012a87d35a483af278699980776fc0bca0990a60ad3fd9a303904de32f 1.37kB / 1.37kB                                                     0.0s
 => => sha256:eb8b8b8a361056a1107428997a0c13a18c013ad612f24e54cb6990e60bfed3ec 7.02kB / 7.02kB                                                     0.0s
 => => sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96 27.19MB / 27.19MB                                                   0.3s
 => => sha256:a9db6797916ed95aa70dba9828c955247db171807e704ae7b1fb37b7c7e4b0e6 450B / 450B                                                         0.3s
 => => extracting sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96                                                          0.9s
 => => extracting sha256:ecdd21ad91a4e69294555b3e56a71a7382a58a9c54b02d9038bcd3821ba3d072                                                          0.0s
 => => extracting sha256:72f5a0bbd6d5f85fce35070bd624cf69c2ceb91424afe8a5ed2a02442cdd711c                                                          0.8s
 => => extracting sha256:6d65359ecb29ff24f2322d5ad308f0a8a95980706ae2e76315a267474402aa3a                                                          0.1s
 => => extracting sha256:a9db6797916ed95aa70dba9828c955247db171807e704ae7b1fb37b7c7e4b0e6                                                          0.0s
 => [internal] load build context                                                                                                                  0.1s
 => => transferring context: 4.59MB                                                                                                                0.0s
 => [2/6] WORKDIR /app                                                                                                                             0.5s
 => [3/6] RUN mkdir -p /app /.npm /tmp/.npm     && chgrp -R 0 /app /.npm /tmp     && chmod -R g+rwX /app /.npm /tmp                                0.2s
 => [4/6] COPY package*.json ./                                                                                                                    0.1s
 => [5/6] RUN npm install --legacy-peer-deps                                                                                                      20.4s
 => [6/6] COPY . .                                                                                                                                 0.0s 
 => exporting to image                                                                                                                             2.1s 
 => => exporting layers                                                                                                                            2.1s 
 => => writing image sha256:3784f9a2cf74b04915cf5354e75cd9a2529b6cdf60c91cf2381c0c79ecfaa841                                                       0.0s 
 => => naming to docker.io/library/swiggy-nodejs-app                                                                                               0.0s 
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]# docker run -d -p 3000:3000 swiggy-nodejs-app                                                                                                                                                        
d7fb19de4101700db4036103acb17bdbaa480b0a3029dde84e3159b73d588669
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]# vi dockerfile
[root@ip-172-31-11-187 swiggy-nodejs-devops-project]#
  ```
# copy instance pubic ip with port no.
    <public IP>:port number
     100.126.28.212:5000     


  --> then enter
<img width="1912" height="496" alt="Screenshot 2025-12-03 164533" src="https://github.com/user-attachments/assets/0c549ac5-b9b1-455f-a64e-12fa25c5d3c6" />
