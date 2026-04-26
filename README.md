# aws-s3-cloudfront-static-website
## Description : 
This project is divided into 2 parts. 
   - Part 1: Where i have created a static website and hosted it on the internet with Amazon S3
   - Part 2: The same website I have hosted on internet using Amazon S3 + Cloudfront
##
First of all I created an IAM User 'AdminRP' from the root account.
  - IAM - Created IAM Admin User
    - <img width="2810" height="1588" alt="tempImageRhxrWm" src="https://github.com/user-attachments/assets/e152b36a-2ff2-40ea-a9d7-3c06a37853e9" />
  - Signed in using the admin credentials
    - <img width="1402" height="826" alt="Screenshot 2026-04-25 at 12 27 48 PM" src="https://github.com/user-attachments/assets/aaea253d-62a5-416c-91f0-1726de60e24b" />
  - HTML Doc: index.html used which I have saved in the HTML-Doc folder
## 

# Part 1 : Static website delivering with only Amazon S3
   <img width="314" height="468" alt="Screenshot 2026-04-26 at 8 32 30 AM" src="https://github.com/user-attachments/assets/7fe9d827-7098-4819-8a84-c2ebc6c15067" />


- Created S3 bucket (while creating it I unchecked the box for Blocking all public access)
   - <img width="947" height="394" alt="Screenshot 2026-04-25 at 2 25 59 PM" src="https://github.com/user-attachments/assets/ecf5c041-dcca-445a-8fc8-9e488d15abea" />
- Uploaded index.html as object in the bucket created
   - <img width="1409" height="618" alt="Screenshot 2026-04-25 at 2 26 55 PM" src="https://github.com/user-attachments/assets/a255943d-01da-4538-9a74-1b43f9a8e66d" />
- Properties of object showing the public URL of the html file
   - <img width="1404" height="608" alt="Screenshot 2026-04-25 at 2 27 26 PM" src="https://github.com/user-attachments/assets/6262f60e-6b61-417a-8c05-87a908bdac1f" />
- Access being denied as the object is not ready for public access
   - <img width="1440" height="181" alt="Screenshot 2026-04-25 at 2 27 49 PM" src="https://github.com/user-attachments/assets/9cac8e4f-42b1-43db-967d-7872035068d1" />
- Choosing all the objects in the bucket and selecting Permissions to make changes for public access
   - <img width="1415" height="405" alt="Screenshot 2026-04-25 at 2 34 27 PM" src="https://github.com/user-attachments/assets/ac644a54-8f6c-4a56-9bee-fcc3bb997cd0" />
- Changing the ACL from disabled to enabled and acknowledging it. 
   - <img width="1398" height="755" alt="Screenshot 2026-04-25 at 2 35 43 PM" src="https://github.com/user-attachments/assets/e776995c-7206-494b-9c4e-ff663d5fbcba" />
- Selecting my object to make it accessible to public by choosing the Actions>MakePublic using ACL
   - <img width="1425" height="756" alt="Screenshot 2026-04-25 at 2 36 27 PM" src="https://github.com/user-attachments/assets/942614df-e7b1-4720-b99d-886fc4958088" />
   - <img width="1422" height="437" alt="Screenshot 2026-04-25 at 2 36 52 PM" src="https://github.com/user-attachments/assets/9ffce928-11e0-4524-87ab-054e114e59aa" />
- Final check
   - <img width="1414" height="407" alt="Screenshot 2026-04-25 at 2 37 12 PM" src="https://github.com/user-attachments/assets/ec0c2af3-7c90-4906-9e8b-2df4f3a24efc" />
- And our website is now publically accessible
   - <img width="1440" height="463" alt="Screenshot 2026-04-25 at 2 58 57 PM" src="https://github.com/user-attachments/assets/8ba18579-5c22-46bd-9755-d7d357bb0f9f" />
##
   **** Used Claude to audit the project. Understood that ACL based public access was deprecated by AWS in 2023 and for all public access control only bucket policies are sufficient. Hence continuing Part-1 of this project to check the same i.e. without using ACLs.
##
- Created another bucket 'demo-bucket-1.2' 
   - <img width="1419" height="434" alt="Screenshot 2026-04-26 at 6 49 20 AM" src="https://github.com/user-attachments/assets/5a2e5748-e086-4885-8abb-0b3d71d1ee2d" />
- First & foremost the block all public access checbox needs to be unchecked so that we can implement our bucket policy to have access to our object index.html 
   - <img width="1418" height="603" alt="Screenshot 2026-04-26 at 7 19 33 AM" src="https://github.com/user-attachments/assets/1ed7591c-3c82-4d4f-929e-b70f32c4e39c" />
   ### Creating bucket policy for the website hosting
   - <img width="1408" height="759" alt="Screenshot 2026-04-26 at 6 58 02 AM" src="https://github.com/user-attachments/assets/f3c2caf4-35ae-43d2-931c-fcfa40fc53e4" />
   - Clicked on Add new statement and chose S3 from the All services option on the left
      - <img width="1410" height="720" alt="Screenshot 2026-04-26 at 7 09 49 AM" src="https://github.com/user-attachments/assets/9e0e1f95-809f-46a0-8a14-a5f3b8ca9f99" />
   - Added GetObject action in the Add Actions bar
      - <img width="1375" height="709" alt="Screenshot 2026-04-26 at 7 13 40 AM" src="https://github.com/user-attachments/assets/0729fa36-47fb-4c9b-8c4a-bf976e548766" />
   - Mentioned the details about the resources (bucket name & object name)
      -<img width="1402" height="720" alt="Screenshot 2026-04-26 at 7 15 48 AM" src="https://github.com/user-attachments/assets/f2995a32-204d-47f4-b04e-e37642eb5d42" />
   - Finally our JSON policy is completed with the object index.html having the public access
      - <img width="1390" height="702" alt="Screenshot 2026-04-26 at 7 26 30 AM" src="https://github.com/user-attachments/assets/22846499-884e-4f61-b1af-9f27544aba7d" />
   - Copied the URL of our object index.html
      - <img width="1395" height="564" alt="Screenshot 2026-04-26 at 7 29 09 AM" src="https://github.com/user-attachments/assets/ed3f14b3-a257-4465-a294-0a0c780a8806" />
   - And finally our static website index.html is hosted
      - <img width="1440" height="900" alt="Screenshot 2026-04-26 at 7 30 04 AM" src="https://github.com/user-attachments/assets/20a7a84d-878f-4301-9ac0-dc55740f99a2" />










