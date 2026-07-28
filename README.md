# Application-Deployment3
Final Project

Step 1 Create an t2 micro EC2 Instance with 20GB of configure storage with 

 Type        Port  Source                                                      
 --------------------------------------------------------------------------- 
 SSH         22    Anywhere (0.0.0.0/0)                                   
 HTTP        80    Anywhere (0.0.0.0/0)                                   
 Custom TCP  8080  My IP 

<img width="1918" height="816" alt="image" src="https://github.com/user-attachments/assets/b1de1f67-c6d1-4c33-b5ab-c749fc87816c" />

Step 2 We'll install: Git /Docker /Docker Compose /Java /Jenkins

<img width="677" height="190" alt="image" src="https://github.com/user-attachments/assets/bd6f0027-28b7-4c0a-a55f-371631b31ef1" />
<img width="1905" height="822" alt="image" src="https://github.com/user-attachments/assets/e7fbc6ae-650d-4d69-80c1-d1eb4a23ff19" />
<img width="1911" height="126" alt="image" src="https://github.com/user-attachments/assets/164028f3-d0f8-4583-8f12-584ef2069a97" />
<img width="967" height="167" alt="image" src="https://github.com/user-attachments/assets/b851f88c-d675-44ea-af76-eb7e5d4a437f" />
<img width="1088" height="377" alt="image" src="https://github.com/user-attachments/assets/c276ceb4-9373-4abd-bf97-11a1023fa287" />
<img width="1897" height="813" alt="image" src="https://github.com/user-attachments/assets/846afd45-be4d-468b-89ec-78e45a803b38" />
<img width="1897" height="983" alt="image" src="https://github.com/user-attachments/assets/35dc8a60-77e8-46e8-b7e7-817ceeac5e2b" />
<img width="1912" height="842" alt="image" src="https://github.com/user-attachments/assets/a4d32e5c-b2be-4ca2-8d8c-00151b781abc" />

Step 3 Clone Project and create Dockerfile
<img width="692" height="117" alt="image" src="https://github.com/user-attachments/assets/f7be100d-f793-402f-b964-d5350f2ccea3" />
<img width="1912" height="823" alt="image" src="https://github.com/user-attachments/assets/5f3af4be-e8ec-4574-8213-5ddb90194111" />

Step 4 Build Docker Image run the container and verify using public ip
<img width="1900" height="813" alt="image" src="https://github.com/user-attachments/assets/128ea492-8ad9-430f-81aa-dea33626709f" />
<img width="1327" height="182" alt="image" src="https://github.com/user-attachments/assets/651d60c3-52a3-4f4f-84e1-13b270488a7c" />
<img width="1907" height="988" alt="image" src="https://github.com/user-attachments/assets/d5556ea2-630e-49fe-9da2-8a259024b758" />

Step 5 Create a docker-compose.yml Write build.sh deploy.sh but 
Since we let Docker Compose manage the container first stop and remove the manually created one

<img width="1310" height="283" alt="image" src="https://github.com/user-attachments/assets/0a4ac7db-04b9-4047-a5ca-570d1f5246c5" />
<img width="1660" height="822" alt="image" src="https://github.com/user-attachments/assets/2cc2ccf7-c415-48ab-9c35-0a2e3a858010" />

Check docker-compose will create the container
<img width="1417" height="290" alt="image" src="https://github.com/user-attachments/assets/d558ad48-e9a8-4554-a156-49f1a6195e1b" />
This will ensure later jenkins will only run docker compose up -d instead of going through long docker run easier to maintain and scales better

Step 6 Create build.sh and deploy.sh and give execute permission chmod +x to build docker image and deploy Docker conatainer

<img width="1183" height="817" alt="image" src="https://github.com/user-attachments/assets/f7a58dab-a5ab-4a0b-ae4d-cdeab23d7054" />
<img width="832" height="818" alt="image" src="https://github.com/user-attachments/assets/47556b10-244b-4c47-ad26-ac80bf39d5d5" />
Create .dockerignore and .gitignore and test ./build.sh

<img width="787" height="811" alt="image" src="https://github.com/user-attachments/assets/0ce872fc-2f52-4e74-a65d-efccdc825829" />
<img width="676" height="781" alt="image" src="https://github.com/user-attachments/assets/1567b134-c7f4-435d-ae82-ff62756b3013" />

Step 7 Check git status Create Dev Branch and Commit the Docker Work
<img width="752" height="327" alt="image" src="https://github.com/user-attachments/assets/84fc4bd1-6dc3-4afd-bec9-c0e255fca5b7" />
<img width="980" height="648" alt="image" src="https://github.com/user-attachments/assets/cc095ae5-4adc-4f6d-9e0b-1c610646a2df" />
<img width="1262" height="501" alt="image" src="https://github.com/user-attachments/assets/778a41d0-02ca-4ce5-8653-2cf17a4f462a" />
<img width="1891" height="753" alt="image" src="https://github.com/user-attachments/assets/53aaf4f0-8748-4518-afab-b34eb55a230a" />

Step 8 Login Docker Hub from EC2 

<img width="1030" height="408" alt="image" src="https://github.com/user-attachments/assets/0cdd7c64-2de8-48ea-a3ca-375d3a153d6c" />

Modify build.sh and build and verify dockerhub

<img width="665" height="757" alt="image" src="https://github.com/user-attachments/assets/dd69fc1e-9176-4197-b434-692237be5568" />
<img width="1362" height="785" alt="image" src="https://github.com/user-attachments/assets/b6c632ed-018e-48ff-ac3d-214c9f22d4b6" />
<img width="1335" height="700" alt="image" src="https://github.com/user-attachments/assets/17e7d806-ae48-43b5-95f8-16128759f7ef" />
<img width="1250" height="757" alt="image" src="https://github.com/user-attachments/assets/0cb62e45-a394-47cb-a26c-da44dfbc3370" />

Step 9 Give Jenkins permission to use Docker

<img width="1490" height="198" alt="image" src="https://github.com/user-attachments/assets/b46cf194-ae15-4014-9bf1-cdeb534b7f42" />
<img width="1482" height="273" alt="image" src="https://github.com/user-attachments/assets/a2c2c113-86ca-41c7-bdd1-e18045dff26a" />

Step 10 Install Jenkins necessary Plugins and add dockerhub credintials
<img width="1901" height="862" alt="image" src="https://github.com/user-attachments/assets/d3d0d952-4ab2-4f97-bb2f-60d27a820da0" />
<img width="1888" height="967" alt="image" src="https://github.com/user-attachments/assets/ea1c6046-a9c1-477b-81c3-4b78ff017bae" />

Step 11 Create Jenkins Pipeline (DEV branch)

<img width="1887" height="881" alt="image" src="https://github.com/user-attachments/assets/3c40bfba-8c4e-449d-957f-5d8d51576fcd" />
<img width="1387" height="941" alt="image" src="https://github.com/user-attachments/assets/93d05e2e-a2c2-48cd-bc41-f0f5518d6546" />

<img width="1887" height="887" alt="image" src="https://github.com/user-attachments/assets/ea5e7314-58cf-43e3-9b3b-e9c3e2a4147c" />

ADD Webhook
<img width="1862" height="847" alt="image" src="https://github.com/user-attachments/assets/87512607-1adb-4939-ba5d-371a2012ec84" />
Testing  Jenkins Build to check CI pipeline
<img width="1862" height="820" alt="image" src="https://github.com/user-attachments/assets/cb7fb8c8-6b1c-4960-9686-14c5e226a63b" />
<img width="1588" height="590" alt="image" src="https://github.com/user-attachments/assets/a3f88b8b-6811-477e-b6bd-3e5abca7a7a5" />


create the master branch  the Production Pipeline :

<img width="1887" height="897" alt="image" src="https://github.com/user-attachments/assets/71d5c44e-98ba-4346-9d1c-879a4bd8d32f" />
<img width="1317" height="917" alt="image" src="https://github.com/user-attachments/assets/f51f9392-ed78-45e4-95b1-9ef29c8949d2" />
<img width="1902" height="897" alt="image" src="https://github.com/user-attachments/assets/14ed217a-752b-452c-91e6-05d327043ab7" />

Test the Production Pipeline
Merge  dev branch into main:
<img width="1207" height="711" alt="image" src="https://github.com/user-attachments/assets/6d2723ec-9948-43f3-b4fe-3e5a51476bc7" />
<img width="1090" height="642" alt="image" src="https://github.com/user-attachments/assets/4ca1018c-9fa6-400d-b357-c87f87ee5d75" />

Build The CI/CD pipeline using main branch 
<img width="1907" height="857" alt="image" src="https://github.com/user-attachments/assets/23460d07-b4de-4644-ac2e-048b3b61bf3a" />
<img width="1910" height="772" alt="image" src="https://github.com/user-attachments/assets/c84bf165-089b-4988-ae73-65de8f9343ce" />
<img width="1892" height="670" alt="image" src="https://github.com/user-attachments/assets/c91d3ab7-7240-492a-9cdf-145d4fa0892c" />



Step 12 Using open-source monitoring system Uptime Kuma open port 3001 TCP my IP

<img width="762" height="825" alt="image" src="https://github.com/user-attachments/assets/49fba748-cb9f-4295-baba-22e3463968f7" />
<img width="1635" height="262" alt="image" src="https://github.com/user-attachments/assets/932073c5-64b5-4911-a534-703d2d19c2db" />

Add new monitor with public Ip and set notifications Email(SMTP) from settings 

<img width="1892" height="742" alt="image" src="https://github.com/user-attachments/assets/7c6cb757-051d-4aeb-90a4-9845c97a87ea" />
<img width="1753" height="863" alt="image" src="https://github.com/user-attachments/assets/d23ef12c-595c-41e4-aa59-cf80dd388e6e" />
<img width="1890" height="881" alt="image" src="https://github.com/user-attachments/assets/036e7dec-89d5-4475-8484-10f7181ebbbe" />
<img width="337" height="132" alt="image" src="https://github.com/user-attachments/assets/ab3da624-a348-4b20-8830-f0eba5009766" />
<img width="1893" height="806" alt="image" src="https://github.com/user-attachments/assets/315a879b-477e-4cad-84a6-bc4aff71ce10" />

