# EmailJS Setup Guide

This guide will help you set up EmailJS for your portfolio contact form.

## Step 1: Create EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

## Step 2: Add Email Service

1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail, Outlook, Yahoo, etc.)
4. Follow the setup instructions for your provider
5. Note down your **Service ID**

### Gmail Setup
- Select Gmail
- Click "Connect Account"
- Sign in with your Gmail account
- Allow EmailJS permissions

### Outlook Setup
- Select Outlook
- Enter your email and password
- Complete the verification process

## Step 3: Create Email Template

1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template structure:

```
Subject: Portfolio Contact: {{subject}}

From: {{from_name}}
Email: {{from_email}}

Message:
{{message}}

---
This message was sent from your portfolio website.
```

4. Save the template and note down your **Template ID**

## Step 4: Get Your Public Key

1. Go to "Account" in your dashboard
2. Find your **Public Key** (also called User ID)
3. Copy this key

## Step 5: Update Your Code

Replace the placeholders in your `script.js` file:

```javascript
// Initialize EmailJS with your public key
emailjs.init('YOUR_PUBLIC_KEY_HERE');

// In the ContactFormManager class, update the send method:
await emailjs.send('YOUR_SERVICE_ID_HERE', 'YOUR_TEMPLATE_ID_HERE', templateParams);
```

## Step 6: Test Your Form

1. Open your portfolio website
2. Fill out the contact form
3. Submit the form
4. Check your email to confirm it works

## Template Variables

Your EmailJS template can use these variables from the contact form:

- `{{from_name}}` - The sender's name
- `{{from_email}}` - The sender's email address
- `{{subject}}` - The email subject
- `{{message}}` - The message content

## Example Template

Here's a more detailed template example:

```
Subject: New Portfolio Contact - {{subject}}

Hello!

You have received a new message from your portfolio website.

Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This email was automatically sent from your portfolio contact form.
Sent on {{sent_date}}
```

## Troubleshooting

### Form Not Sending
- Check your Service ID, Template ID, and Public Key are correct
- Ensure your email service is properly connected
- Check the browser console for error messages

### Emails Going to Spam
- Add your portfolio domain to your email's safe sender list
- Consider using a custom "from" email address in your service settings

### Rate Limiting
- EmailJS free plan has a monthly limit
- Consider upgrading if you exceed the limit

## Security Best Practices

1. **Never expose your Private Key** - Only use the Public Key in frontend code
2. **Use template variables** - Don't concatenate user input directly
3. **Validate input** - The portfolio already includes form validation
4. **Monitor usage** - Check your EmailJS dashboard regularly

## Alternative Email Services

If you prefer other services, you can also use:
- [Formspree](https://formspree.io/)
- [Netlify Forms](https://www.netlify.com/products/forms/)
- [Getform](https://getform.io/)

## Support

If you encounter issues:
1. Check the [EmailJS Documentation](https://www.emailjs.com/docs/)
2. Visit their [FAQ section](https://www.emailjs.com/docs/faq/)
3. Contact EmailJS support through their dashboard

---

Once you've completed these steps, your portfolio contact form will be fully functional!

