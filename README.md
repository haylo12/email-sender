# email-sender
 This is a scripty to send emails
 
  import smtplib                                                                   
  from email.message import EmailMessage                                          
  from string import Template                                     
  from pathlib import Path                                              

html = Template(Path("index.hmtl").read_text())                        
email = EmailMessage()                                       
email["from"] = "username"                                                    
email["to"] = "#"                                        
email["subject"] = "you won 1,000,000 dollars!"                                                 

email.set_content("I  am a Python Master!")                                                               

with smtplib.SMTP(host="smtp.gmail.com", port=587) as smtp:                                               
    smtp.ehlo()                                             
    smtp.starttls()                                                         
    smtp.login("#", "#")                                                                   
    smtp.send_message(email)                                                                   
    print("all good boss!")
