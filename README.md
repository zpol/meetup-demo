# meetup-demo


As was commented on the TechTalk presentation, this repository shows as an example how you can build your own Countinuous Delivery platform by using __[drone-server](https://github.com/drone/drone)__ and __[gogs](gogs.io)__ an alternative to Jenkins,spinnaker among others CI/CD platforms. 100% Opensource, written in go and container native! :D  


![alt text](https://github.com/zpol/meetup-demo/raw/master/img/gogs.png "Gogs")

![alt text](https://github.com/zpol/meetup-demo/raw/master/img/drone.png "Drone-server")

![alt text](https://github.com/zpol/meetup-demo/raw/master/img/drone2.png "Drone-server")




---

## How it works 

To run this DEMO you just need [Docker Engine](https://docs.docker.com/engine/) installed and [Docker Compose](https://docs.docker.com/compose/
). 

To run the demo just download this repo: 

```
git clone https://github.com/zpol/meetup-demo
```
Then type: 

```
cd meetup-demo && docker-compose up 
```

This will start all the stack by using the parameters set into the [docker-compose.yml](https://github.com/zpol/meetup-demo/blob/master/docker-compose.yml) file 

When everything is up and running you will have: 

* A MySQL container called __db__ containing all the gogs configuration and settings listenning on port 3306/tcp
* A Drone-Server container named **drone-server** listenning on port 8000/tcp
* And a Gogs server named **gogs** listenning on port 3000/tcp 

In fact you just need to connect via http to: 

**Gogs:** http://localhost:3000 

and 

__Drone:__ http://localhost:8000 

to access the two different GUIs for each software.

## Different scenarios

__Local development environment:__

You can just install Docker Engine in your laptop or workstation and run the demo. You will have your own git platform and drone-server up and running in secconds. 

__Remote developemnt environment:__ (i.e.: AWS, Google Cloud, Azure,...)

There are several ways to deploy a production Continuous Delivery platform by using this demo: ECR; ECS, EC2, EKS,... 

To simplify you can start by running an EC2 instance and install Docker Engine and Docker Compose.
If you don't want to install it manually there's also a Launch configuration just ready to use [here](https://github.com/zpol/meetup-demo/blob/master/examples/EC2_Launch_Configuration.txt)

If you want more, (resilience, fault tolerancy, hight availability and so on...) the you should consider launch this stack in a more complex way.

***NOTE: If you're going to build this into the cloud, don't forget to change ALL the access credentials!!***



----------------------------------


## License



The repository utilizes code licensed under the terms of the Apache Software License and therefore is licensed under ASL v2 or later.

This source code in this repository is free: you can redistribute it and/or modify it under the terms of the Apache Software License version 2, or (at your option) any later version.

This soruce code in this repository is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the Apache Software License for more details.

You should have received a copy of the Apache Software License along with this program. If not, see http://www.apache.org/licenses/LICENSE-2.0.html

The source code forked from other open source projects will inherit its license.

## Privacy
This repository contains only non-sensitive, publicly available data and information. All material and community participation is covered by the Surveillance Platform Disclaimer and Code of Conduct. For more information about CDC's privacy policy, please visit http://www.cdc.gov/privacy.html.

## Contributing
Anyone is encouraged to contribute to the repository by forking and submitting a pull request. (If you are new to GitHub, you might start with a basic tutorial.) By contributing to this project, you grant a world-wide, royalty-free, perpetual, irrevocable, non-exclusive, transferable license to all users under the terms of the Apache Software License v2 or later.

All comments, messages, pull requests, and other submissions received through CDC including this GitHub page are subject to the Presidential Records Act and may be archived. Learn more at http://www.cdc.gov/other/privacy.html.

