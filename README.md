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



# CloudFront Distribution Setup

## 1. Access and Create Distribution

1. **Access CloudFront**:  
   In the AWS Management Console, navigate to the CloudFront service.  
   ![image](https://github.com/user-attachments/assets/1e3df9cb-5384-4cec-810f-294540b482f6)


2. **Create a New Distribution**:  
   Click on `Create Distribution` and choose the `Web` option for distribution.

   ![image](https://github.com/user-attachments/assets/ee76cbfd-51fa-4e22-ad8a-decce9012ddd)


---

## 2. Configure Origin and Viewer Settings

1. **Origin Domain Name**:  
   Select your S3 bucket from the dropdown list in the origin configuration section.

2. **Origin Path (Optional)**:  
   If you want to restrict access to specific content, specify the path within your S3 bucket.

3. **Viewer Protocol Policy**:  
   Choose whether to allow both HTTP and HTTPS or enforce a redirect from HTTP to HTTPS for secure content delivery.

---

## 3. Configure and Deploy the Distribution

1. **Cache Behavior Settings**:  
   Adjust how CloudFront caches content, including request handling and object caching duration.  


2. **Distribution Settings**:  
   Choose your pricing class, add alternate domain names (CNAMEs) if needed, and configure SSL certificates for custom domains.

3. **Review and Deploy**:  
   After reviewing your settings, click `Create Distribution`. Deployment may take some time. Once complete, you'll receive a CloudFront domain name.

   ![image](https://github.com/user-attachments/assets/55c2a766-2205-45ee-925d-52855eabe2c2)


   When you click on your CloudFront distribution, you can copy your website url which is **Distribution Domain Name**

   ![image](https://github.com/user-attachments/assets/f734ca3a-e215-4567-af83-77bbf2cb4b62)
   
 My website is now available with cloudFrond

 ![image](https://github.com/user-attachments/assets/9c03a9b9-914b-4fdc-98d4-b7a1aad36216)
