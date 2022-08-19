# Cloud computing

Requirements for a machine

- OS windows 10/11 - ubuntu bionic16.04LTS - Vagrant box online
- Processor
- RAM
- SSD - storage - volume
- Hard Drive
- Graphic Card
- Power Supply
- CPU
- Motherboard
- Touch Screen
- Firewall - Security tool
- Quality

  ![Screenshot 2022-08-18 at 14 54 54](https://user-images.githubusercontent.com/102330725/185412693-c6258b14-15be-4082-9943-eeade718f781.png)

## Step up AWS EC2 service

1. Search for EC2 service on AWS

<img width="1108" alt="Screenshot 2022-08-18 at 19 12 17" src="https://user-images.githubusercontent.com/102330725/185465681-ca09715b-2782-4624-81d0-4a822b4d6475.png">

2. Go to launch instance and select 'Launch Instance' from the dropdown

![Screenshot 2022-08-18 at 17 55 58](https://user-images.githubusercontent.com/102330725/185465923-6fb8eb58-40ad-417b-ad41-ae37387a6243.png)

3. Choose Ubuntu Server as Amazon Machine Image

![Screenshot 2022-08-18 at 17 56 39](https://user-images.githubusercontent.com/102330725/185466424-c1df9521-dc9f-4568-a569-0053dad10969.png)

4. Select **t2 micro** as the Instance Type

![Screenshot 2022-08-18 at 17 56 58](https://user-images.githubusercontent.com/102330725/185466552-4c6097a3-0d2c-44bb-80fd-e238b8bb244c.png)

5. Configure Instance Details

![Screenshot 2022-08-18 at 17 57 37](https://user-images.githubusercontent.com/102330725/185472465-e7ddbe1a-c69d-4c3a-8223-323f6ef57d1c.png)

6. Add Storage

![Screenshot 2022-08-18 at 17 58 15](https://user-images.githubusercontent.com/102330725/185472573-9e7a435d-1f5b-48ac-b186-88c06d6d78a9.png)

7. Add Tags

![Screenshot 2022-08-18 at 17 58 59](https://user-images.githubusercontent.com/102330725/185472674-fea0cc45-2692-4108-8b90-87e9d26d7119.png)

8. Configure security groups

- HTTP
- SSH
- Port 3000

![Screenshot 2022-08-18 at 17 59 51](https://user-images.githubusercontent.com/102330725/185473103-0a2adf14-6712-447d-844d-d4612e01f190.png)

**In the terminal**, navigate to `~/.ssh`, run `chmod 400 keyname` to ensure that the key can't be viewed publicly.
Copy the command below from Connect to Instance --> SSH Client, and run in the SSH folder in terminal.

![Screenshot 2022-08-18 at 18 00 41](https://user-images.githubusercontent.com/102330725/185477425-77a95fe3-c51e-4a3f-b795-e71c207eb320.png)

## Install all required dependencies

```
# update
sudo apt-get update -y

# upgrade
sudo apt-get upgrade -y

# install nginx
sudo apt-get install nginx -y
sudo systemctl status nginx

```

## Migrate files from local host to remote host

`scp -i [key_name] -r [file_source_path] [file_destination_path]`

Run command `sudo scp -i ~/.ssh/eng122.pem -r app/ ubuntu@54.194.205.145:~/app/`

## Install node dependencies

```
# install nodejs
sudo apt-get install nodejs -y

# install version 6
sudo apt-get purge nodejs npm
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -

# install node.js again
sudo apt-get install nodejs -y

# install npm
sudo apt-get install npm -y

# install pm2
sudo npm install pm2 -g

# update
sudo apt-get update -y

#upgrade
sudo apt-get upgrade -y
```

## Configure reverse proxy

- Create proxy_file

```
server {
        listen 80 default_server;
        listen [::]:80 default_server;

        root /var/www/html;


        index index.html index.htm index.nginx-debian.html;

        server_name _;

        location / {
                proxy_pass http://localhost:3000;
        }
}
```

Run commands

`sudo cp -f proxy_file /etc/nginx/sites-available/default`

`sudo systemctl restart nginx`

`systemctl status nginx`

## Start App

- Run `npm install`
- Run `npm start`

- Go to Connect to Instance and copy the Public IP address. Paste it on browser and the app should be working.


![Screenshot 2022-08-18 at 18 00 49](https://user-images.githubusercontent.com/102330725/185482425-b269ba7a-7670-4021-b94e-38499100220e.png)

## To connect the app to the DB

- Create an instance of the DB following the same steps as for the app
- Add Port 27017 to the inbound rules of in the DB instance

<img width="1184" alt="Screenshot 2022-08-19 at 17 18 38" src="https://user-images.githubusercontent.com/102330725/185665254-30e0a81f-33f8-48e6-ae92-f470d936474c.png">

- Once the instance is created, Go to Connect --> SSH Client and copy the code. Run the copied code in the `~/.ssh` folder in the terminal.
<img width="798" alt="Screenshot 2022-08-19 at 17 21 14" src="https://user-images.githubusercontent.com/102330725/185665492-1bc64476-0c72-440e-9411-4cb20108f9ff.png">

## Cloud Computing and various Services

![Slide1](https://user-images.githubusercontent.com/102330725/185626395-b3389d46-05e1-441d-b6ba-07f6ea7cc75d.jpg)

![Slide2](https://user-images.githubusercontent.com/102330725/185626437-8386188e-2851-4146-8496-3c24c27d292f.jpg)

![Slide3](https://user-images.githubusercontent.com/102330725/185626577-28d81745-c2aa-4679-a564-2c91542303c0.jpg)

![Slide4](https://user-images.githubusercontent.com/102330725/185626626-a5b5974c-2778-40f1-bb25-7745d2c7225f.jpg)

![Slide5](https://user-images.githubusercontent.com/102330725/185626668-ec3d58b7-fd21-4dcb-808d-d1b0c83a3681.jpg)

![Slide6](https://user-images.githubusercontent.com/102330725/185626720-18c8c273-3d25-45b5-b174-a74a11925c31.jpg)

![Slide7](https://user-images.githubusercontent.com/102330725/185626755-7ff09fc1-0f33-45f3-812d-bb65a271d8ea.jpg)

![Slide8](https://user-images.githubusercontent.com/102330725/185626820-f4ef177a-682c-48ee-8a35-73f41e49b763.jpg)
