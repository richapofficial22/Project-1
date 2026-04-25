# Project-1
## Description of Project : A static portfolio/resume page hosted on AWS S3, delivered without & with CloudFront CDN with HTTPS. ##
## Services used : 
  - IAM - Created IAM Admin User
    - <img width="2810" height="1588" alt="tempImageRhxrWm" src="https://github.com/user-attachments/assets/e152b36a-2ff2-40ea-a9d7-3c06a37853e9" />
  - Signed in using the admin credentials
    - <img width="1402" height="826" alt="Screenshot 2026-04-25 at 12 27 48 PM" src="https://github.com/user-attachments/assets/aaea253d-62a5-416c-91f0-1726de60e24b" />
  - HTML Doc: index.html used 
## Static website delivering without using CloudFront
- Created bucket (while creating it I unchecked the box for Blocking all public access)
<img width="947" height="394" alt="Screenshot 2026-04-25 at 2 25 59 PM" src="https://github.com/user-attachments/assets/ecf5c041-dcca-445a-8fc8-9e488d15abea" />
- uploaded index.html as object in the bucket created
<img width="1409" height="618" alt="Screenshot 2026-04-25 at 2 26 55 PM" src="https://github.com/user-attachments/assets/a255943d-01da-4538-9a74-1b43f9a8e66d" />
- Properties of object showing the public URL of the html file
<img width="1404" height="608" alt="Screenshot 2026-04-25 at 2 27 26 PM" src="https://github.com/user-attachments/assets/6262f60e-6b61-417a-8c05-87a908bdac1f" />
- Access being denied as the object is not ready for public access
<img width="1440" height="181" alt="Screenshot 2026-04-25 at 2 27 49 PM" src="https://github.com/user-attachments/assets/9cac8e4f-42b1-43db-967d-7872035068d1" />
- Choosing all the objects in the bucket and selecting Permissions to make changes for public access
<img width="1415" height="405" alt="Screenshot 2026-04-25 at 2 34 27 PM" src="https://github.com/user-attachments/assets/ac644a54-8f6c-4a56-9bee-fcc3bb997cd0" />
- Changing the ACL from disabled to enabled and acknowledging it. 
<img width="1398" height="755" alt="Screenshot 2026-04-25 at 2 35 43 PM" src="https://github.com/user-attachments/assets/e776995c-7206-494b-9c4e-ff663d5fbcba" />
- Selecting my object to make it accessible to public by choosing the Actions>MakePublic using ACL
<img width="1425" height="756" alt="Screenshot 2026-04-25 at 2 36 27 PM" src="https://github.com/user-attachments/assets/942614df-e7b1-4720-b99d-886fc4958088" />
<img width="1422" height="437" alt="Screenshot 2026-04-25 at 2 36 52 PM" src="https://github.com/user-attachments/assets/9ffce928-11e0-4524-87ab-054e114e59aa" />
- Final check
<img width="1414" height="407" alt="Screenshot 2026-04-25 at 2 37 12 PM" src="https://github.com/user-attachments/assets/ec0c2af3-7c90-4906-9e8b-2df4f3a24efc" />
- And our website is now publically accessible
<img width="1440" height="463" alt="Screenshot 2026-04-25 at 2 58 57 PM" src="https://github.com/user-attachments/assets/8ba18579-5c22-46bd-9755-d7d357bb0f9f" />



