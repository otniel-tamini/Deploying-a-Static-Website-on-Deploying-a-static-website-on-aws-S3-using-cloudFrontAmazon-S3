### Deploying-a-Static-Website-on-Amazon-S3
Deploying a static website on aws S3 using cloudFront

1. ## Create a bucket
   * Give a unique name for the bucket
   * AWS recommends > For Region, we recommend choosing an AWS Region that is geographically close to you. (This reduces latency and costs.)
   ![](general_configuration.png)
   ![](Object_ownership.png)
2. ## Upload the your website files
   - Click on your bucket to open
   - Click on Upload to start the process of uploding 
   - below "Destination" tick Grand public-read-access: to allow access of our website
   - Finally click on upload to upload the files
![image](https://github.com/user-attachments/assets/ed718554-6383-47da-8168-1f5ee1026d82)
![image](https://github.com/user-attachments/assets/de59a7d6-f6c2-433a-b5c0-29093c929713)
![image](https://github.com/user-attachments/assets/c4873993-7d30-473b-b086-81387712fd9e)
   Go to your bucket properties; enable the "**Static website hosting**" and specify "index.html" like **index document**
![image](https://github.com/user-attachments/assets/fc5e5d8b-486a-42da-be9e-18d5dae745ff)
Select the files and click on **Action**; click on **make public using ACL**
![image](https://github.com/user-attachments/assets/88bec1d5-424a-47fa-8a79-d4bb8f3d37c7)

 **You can your website url in your bucket properties then scroll to the bottom**
 My Website is now available

 ![image](https://github.com/user-attachments/assets/5fcd51d9-a8f7-459a-8460-e66897a2824b)



