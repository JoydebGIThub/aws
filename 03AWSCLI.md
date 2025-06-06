## Install the AWS CLI
- go to `https://aws.amazon.com/cli/`
- Download the windows 64
![image](https://github.com/user-attachments/assets/852b01a9-8b0f-487f-8fe7-3304415aaec4)
- After install we can type `aws` and get the `usage`
![image](https://github.com/user-attachments/assets/d018d584-7be4-4e1f-be28-32fcf03fb746)

 ## AWS CLI Configuration:
 - Version check (aws --version)
 - List of all the user (aws iam list-users) -> Unable to locate credentials
 - For configure the credentials
   - Open the root account
   - Go to `Users`
   - Click on the `User name`.
   - Go to `Security credentails`
   - Scroll down (Access Keys(0))
     - Create Access Key
     - Give the purpose in (Use case)
     - Command Line Interface(CLI)
     - Confirmation click
     - Next --> Create Access Key
- We get the `Access Key` and `Secret access key`
![image](https://github.com/user-attachments/assets/4cabd481-625f-4a11-b0a8-40a7979ab6b2)
- Now we open the terminal and write `aws configure`
- Give the `AWS Access Key ID`
- Give the `AWS Secret Access Key`
- Give the `Default region name` from the `Stockholm`
- Enter
![image](https://github.com/user-attachments/assets/a18eaaca-eb5d-45d1-b4a9-99445ef392fe)
- New again we type `aws iam list-users`
![image](https://github.com/user-attachments/assets/d113aaf1-d2a3-4fd6-a434-18307fcde885)

## AWS IAM Best Practices
- Avoid using root account except of account setup.
- Add user to a group and assign permission to group
- Use password policy or MFA. Through 'Account settings' in the left we can modify the `Password policy`
- Use ACCESS KEYS for CLI/SDK
- Never share ACCESS KEYES or Password
- Audit the permission using IAM credential report. Check the user has proper permission or not. We have an tool for that if we scroll in the left we get `Credentail report` and `Download credentail report`




    


