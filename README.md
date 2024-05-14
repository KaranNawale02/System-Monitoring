# System-Monitoring
This is project about system monitoring tool that I have learned. I used Prometheus and Grafana tools for monitoring systems. For monitoring, created two AWS EC2 instances with AmazonLinux OS and as a server used CentOS on local VM.

Firstly start server VM then install and configure the Prometheus and Grafana as per the given step. ( follow the instruction given in the above file )


![prometheus_home_page](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/4d62aa74-5240-45b9-9864-2c610a05a9b4)


![grafana_home_page](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/1962ac05-b273-46f0-825f-6d1bef2fc075)


After the installation, launch the EC2 instances and add the ports 9090 and 9100 in the security group. Port 9090 is used by Prometheus and 9100 is used by node exporter to send the system matix to server.

![security_group_aws](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/83f85743-e0da-45e8-a19a-52f8dd86704a)

Now add the IP of systems that we want to monitor in the server in the file /etc/prometheus/prometheus.yml 

After sussfully add the the IP's restart the daemon process and restart the service Prometheus.
go to browser and hit localhost:9090/targets you will see the following. the IP's will be vary.


![prometheus](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/b6fb2e61-0c6a-4554-b507-b532314257f8)


now add another tab and hit the localhost:3000 this port is used by the grafana. We used grafana for graphical interface. 
go to the dashboard and iport dashboard of id 1860 and select the data source as Prometheus. You will see the following output 



![monitoring_machine_01](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/e4c9e7e3-35d4-41b6-8cd2-e17b3447bbb3)



![monitoring_machine_02](https://github.com/KaranNawale02/System-Monitoring/assets/124289243/9d5f785e-1b51-4e21-8b93-c4093ac6a256)



