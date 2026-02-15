# Email Integration Examples

## How to Use in Your Application

When your admin approves a user, send them an email with a link to the appropriate status page.

### Example 1: User Approval Email

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Account Approved</title>
</head>
<body>
    <h1>Your Account Has Been Approved!</h1>
    <p>Dear User,</p>
    <p>Your account has been approved by the administrator.</p>
    <p>
        <a href="https://fahimsadi.github.io/status/?status=approved">
            Click here to view your approval status
        </a>
    </p>
</body>
</html>
```

### Example 2: Link Expiration Email

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Link Expired</title>
</head>
<body>
    <h1>Verification Link Expired</h1>
    <p>Dear User,</p>
    <p>The verification link you clicked has expired.</p>
    <p>
        <a href="https://fahimsadi.github.io/status/?status=expired">
            Click here to view details
        </a>
    </p>
</body>
</html>
```

### Example 3: Error Notification Email

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Error Processing Request</title>
</head>
<body>
    <h1>Error Processing Your Request</h1>
    <p>Dear User,</p>
    <p>An error occurred while processing your request.</p>
    <p>
        <a href="https://fahimsadi.github.io/status/?status=error">
            Click here to view error details
        </a>
    </p>
</body>
</html>
```

## Backend Integration Examples

### Node.js / Express

```javascript
const nodemailer = require('nodemailer');

async function sendApprovalEmail(userEmail) {
    const transporter = nodemailer.createTransport({
        // your email config
    });

    const mailOptions = {
        from: 'admin@yourcompany.com',
        to: userEmail,
        subject: 'Account Approved',
        html: `
            <h1>Your Account Has Been Approved!</h1>
            <p>Dear User,</p>
            <p>Your account has been approved by the administrator.</p>
            <p>
                <a href="https://fahimsadi.github.io/status/?status=approved">
                    Click here to continue
                </a>
            </p>
        `
    };

    await transporter.sendMail(mailOptions);
}

async function sendExpirationEmail(userEmail) {
    // Similar to above but with status=expired
    const link = 'https://fahimsadi.github.io/status/?status=expired';
    // ... send email with link
}

async function sendErrorEmail(userEmail) {
    // Similar to above but with status=error
    const link = 'https://fahimsadi.github.io/status/?status=error';
    // ... send email with link
}
```

### Python / Flask

```python
from flask_mail import Mail, Message

def send_approval_email(user_email):
    msg = Message(
        'Account Approved',
        sender='admin@yourcompany.com',
        recipients=[user_email]
    )
    
    msg.html = '''
        <h1>Your Account Has Been Approved!</h1>
        <p>Dear User,</p>
        <p>Your account has been approved by the administrator.</p>
        <p>
            <a href="https://fahimsadi.github.io/status/?status=approved">
                Click here to continue
            </a>
        </p>
    '''
    
    mail.send(msg)

def send_expiration_email(user_email):
    # Similar with status=expired
    pass

def send_error_email(user_email):
    # Similar with status=error
    pass
```

### PHP

```php
<?php
function sendApprovalEmail($userEmail) {
    $to = $userEmail;
    $subject = 'Account Approved';
    $message = '
        <html>
        <head><title>Account Approved</title></head>
        <body>
            <h1>Your Account Has Been Approved!</h1>
            <p>Dear User,</p>
            <p>Your account has been approved by the administrator.</p>
            <p>
                <a href="https://fahimsadi.github.io/status/?status=approved">
                    Click here to continue
                </a>
            </p>
        </body>
        </html>
    ';
    
    $headers = "MIME-Version: 1.0" . "\r\n";
    $headers .= "Content-type:text/html;charset=UTF-8" . "\r\n";
    $headers .= 'From: admin@yourcompany.com' . "\r\n";
    
    mail($to, $subject, $message, $headers);
}

function sendExpirationEmail($userEmail) {
    // Similar with status=expired
}

function sendErrorEmail($userEmail) {
    // Similar with status=error
}
?>
```

## Dynamic Status with Additional Parameters

You can also add custom parameters for tracking or customization:

```
https://fahimsadi.github.io/status/?status=approved&user=john&timestamp=1234567890
```

Note: The current implementation only reads the `status` parameter. To use additional parameters, you would need to modify the JavaScript in `index.html` to read and display them.

## QR Code Integration

You can also generate QR codes that link to the status pages:

```python
import qrcode

def generate_approval_qr(user_id):
    url = f'https://fahimsadi.github.io/status/?status=approved'
    qr = qrcode.make(url)
    qr.save(f'approval_qr_{user_id}.png')
```

This allows users to scan a QR code from a printed document to view their status.
