# Project-1
## Description of Project : A static portfolio/resume page hosted on AWS S3, delivered without & with CloudFront CDN with HTTPS. ##
- For this the bucket should have all public access blocked along with the individual objects inside the bucket. 
- go to bucket permissions
  <img width="1418" height="442" alt="Screenshot 2026-04-25 at 3 24 02 PM" src="https://github.com/user-attachments/assets/09253cb4-10a1-49ab-81d3-5684989fa8ca" />
- Under object ownership we choose edit and select ACLs disabled and save the changes made
  <img width="1422" height="442" alt="Screenshot 2026-04-25 at 3 26 01 PM" src="https://github.com/user-attachments/assets/d76ae92c-6bc6-48e0-98e8-2163d3b4c4d8" />
- We change the public access settings by editing the Block Public Access (bucket settings)
  <img width="1404" height="526" alt="Screenshot 2026-04-25 at 3 26 45 PM" src="https://github.com/user-attachments/assets/7dea7bf3-cdd1-4b7f-aa2f-d0cb2e249750" />
- We Block all public access and confirm our changes
<img width="1424" height="572" alt="Screenshot 2026-04-25 at 3 28 09 PM" src="https://github.com/user-attachments/assets/de35696f-0850-40f2-a081-7e5d42f03f8d" />
- Open Cloudfront to create distribution
<img width="1422" height="323" alt="Screenshot 2026-04-25 at 3 32 36 PM" src="https://github.com/user-attachments/assets/11483104-9fad-4add-ae37-e1a6046ff787" />
- I chose the free plan 
  <img width="1413" height="742" alt="Screenshot 2026-04-25 at 3 33 36 PM" src="https://github.com/user-attachments/assets/8c0928ed-421b-49de-ae9f-84c8df100b14" />
-Gave distribution the name d1
  <img width="1399" height="720" alt="Screenshot 2026-04-25 at 3 35 10 PM" src="https://github.com/user-attachments/assets/b05789f9-4e03-4ce3-8787-40eeb1e25774" />
- S3 select kiya and bucket choose kiya
<img width="1399" height="697" alt="Screenshot 2026-04-25 at 3 59 47 PM" src="https://github.com/user-attachments/assets/487bb40b-7e2f-40ea-9e26-b78329cd545e" />
- chose default settings
  <img width="1416" height="558" alt="Screenshot 2026-04-25 at 4 04 14 PM" src="https://github.com/user-attachments/assets/1cb4e84b-84f3-491e-b8d3-de2c91588c82" />
- Reviewed and checked the details
<img width="1405" height="690" alt="Screenshot 2026-04-25 at 4 05 01 PM" src="https://github.com/user-attachments/assets/d4ff5592-c0ab-41a8-a581-2a2052a56887" />
- Finally distribution is created
  <img width="1413" height="704" alt="Screenshot 2026-04-25 at 4 06 15 PM" src="https://github.com/user-attachments/assets/026ab5d4-552e-4892-b025-e4cb7b3e8d0c" />
- we select our bucket to change the origins settings
  <img width="1414" height="750" alt="Screenshot 2026-04-25 at 4 09 20 PM" src="https://github.com/user-attachments/assets/19e63b85-6a90-4dd7-bdc7-6360c99b7a29" />
- We choose origin access control settings to create our policy so that only cloudfront is able to use our static website. 
<img width="1406" height="751" alt="Screenshot 2026-04-25 at 4 10 19 PM" src="https://github.com/user-attachments/assets/5b260ab4-1442-4bb0-b5ca-0632585e948f" />
- Create bucket policy
  <img width="1428" height="797" alt="Screenshot 2026-04-25 at 4 12 26 PM" src="https://github.com/user-attachments/assets/14d6876f-b098-413d-bead-62a1fb30b0c1" />
-Under general settings we just state our default root object and default settings
<img width="1396" height="670" alt="Screenshot 2026-04-25 at 4 17 21 PM" src="https://github.com/user-attachments/assets/5f31a490-d228-4a06-8390-89e0fd93e0cd" />
- we go to S3 and then to our bucket permissions to copy the new json doc or bucket policy which confines our bucket to be used by only cloudfront. Our bucket is still private but it has been given Cloudfront access. 
- <img width="1404" height="752" alt="Screenshot 2026-04-25 at 4 20 40 PM" src="https://github.com/user-attachments/assets/b07cd5a7-2eec-47d3-8ce0-932b8a7c69fa" />

- Finally done with creating distribution
  <img width="1425" height="689" alt="Screenshot 2026-04-25 at 4 28 11 PM" src="https://github.com/user-attachments/assets/aa8bceb3-b70b-4404-af42-7696b59d17f9" />
- And we have our static website running 
  <img width="1440" height="454" alt="Screenshot 2026-04-25 at 4 29 13 PM" src="https://github.com/user-attachments/assets/16afbd7e-e3a8-42cc-b627-2d00e48a5288" />











  

