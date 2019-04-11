# nginx_loadbalancer
nginx loadbalancer with flask backend servers

RUN THESE COMMANDS:
git clone https://github.com/tsachikotek/nginx_loadbalancer.git
CD nginx_loadbalancer
docker-compose up --build

docker ps
docker ps
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS              PORTS                            NAMES
5f186cba3ce5        nginx_loadbalancer_loadbalancer   "nginx -g 'daemon of…"   4 minutes ago       Up 4 minutes        80/tcp, 0.0.0.0:8080->8080/tcp   nginx_loadbalancer_loadbalancer_1_49a4c0def6f6
122d9ef23544        nginx_loadbalancer_backend3       "python app.py"          4 minutes ago       Up 4 minutes                                         nginx_loadbalancer_backend3_1_3b642aa7ffb5
60ad90a7b4df        nginx_loadbalancer_backend1       "python app.py"          4 minutes ago       Up 4 minutes                                         nginx_loadbalancer_backend1_1_8401975aa6bc
aca72a9df57f        nginx_loadbalancer_backend2       "python app.py"          4 minutes ago       Up 4 minutes                                         nginx_loadbalancer_backend2_1_60a329fb18c8

Log:
Successfully built 4f485911a536
Successfully tagged nginx_loadbalancer_loadbalancer:latest
Creating nginx_loadbalancer_backend1_1_25981872ad1e ... done
Creating nginx_loadbalancer_backend2_1_9f2db4b14350 ... done
Creating nginx_loadbalancer_backend3_1_df3ddb512bde ... done
Creating nginx_loadbalancer_loadbalancer_1_b96c0c7fbbe9 ... done
Attaching to nginx_loadbalancer_backend2_1_60a329fb18c8, nginx_loadbalancer_backend1_1_8401975aa6bc, nginx_loadbalancer_backend3_1_3b642aa7ffb5, nginx_loadbalancer_loadbalancer_1_49a4c0def6f6
backend2_1_60a329fb18c8 |  * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
backend2_1_60a329fb18c8 |  * Restarting with stat
backend2_1_60a329fb18c8 |  * Debugger is active!
backend2_1_60a329fb18c8 |  * Debugger PIN: 724-789-804
backend1_1_8401975aa6bc |  * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
backend1_1_8401975aa6bc |  * Restarting with stat
backend1_1_8401975aa6bc |  * Debugger is active!
backend1_1_8401975aa6bc |  * Debugger PIN: 200-819-031
backend3_1_3b642aa7ffb5 |  * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
backend3_1_3b642aa7ffb5 |  * Restarting with stat
backend3_1_3b642aa7ffb5 |  * Debugger is active!
backend3_1_3b642aa7ffb5 |  * Debugger PIN: 320-101-592


reference:
https://codeburst.io/scaling-out-with-docker-and-nginx-8eda9fb1654c
