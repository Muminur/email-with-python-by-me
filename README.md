# email-with-python-by-me
#just give your email password below


simple python program to send email

import smtplib
from email.MIMEMultipart import MIMEMultipart
from email.MIMEText import MIMEText

def emailWarning(msg, msgType):


        fromaddr = 'captainhkr@gmail.com'
        toaddrs = 'mentorpid@gmail.com'
        username = 'captainhkr'
        password = ''
        subj = 'this is me'

        if msgType is 'Info':
                subj = 'this is a subj'

        # Message to be sended with subject field
        message = 'Subject: %s\n\n%s' % (subj,msg)

        # The actual mail sending
        server = smtplib.SMTP('smtp.gmail.com',587)
        server.starttls()
        server.login(username,password)
        server.sendmail(fromaddr, toaddrs, message)
        server.quit()

        return


emailWarning("This is a message", "")


