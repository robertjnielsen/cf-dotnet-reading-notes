# SendGrid

## What Is SendGrid?

[SendGrid](https://sendgrid.com/) is a cloud-based email service that allows us to send emails to users (or whoever) from our applications via an API.

## Use Cases For SendGrid

Some reasons why we would want to use SendGrid (or another service provider if you choose) is that we want to verify information with our users (such as account registration confirmation, email confirmation, password resets, etc).

We could also utilize SendGrid for marketing and newsletter emails.

Just about any reason you could think to send an email to a user, SendGrid is a great service to do so.

## Why Use SendGrid?

Emails are complicated. As users, we think of email from the client perspective (client machine, that is).

Normally, we open an app, or sign in to a web application, and then we can send and recieve emails. Easy, right?

Not so much.

The system administrator in me dies a little whenever having to work with email servers.

They're not **_overly_** complicated to configure in themselves... In fact, some are fairly straightforward (PHP actually has a built in `mail` extension for this purpose).

The problem is that most developers aren't administrators.

We don't want to deal with configuring an email server. We don't want to manage DNS and networking. Not to mention that a custom mail server will not work from home if that's where we choose to develop and test our applications.

Private / residential internet packages across America almost all have ports 25, 587, and 465 blocked. This means that you can't send mail from your home internet.

To do so, you would have to call your Internet Service Provider (ISP) and request they open those ports for you. They probably won't...

They won't for two reasons:

1. They want money. Those ports are open on business internet accounts, which means that if you wanted those ports available at your home, you'd have to change your internet plan to a business plan, which has its pros and cons. It's more expensive (usually, you may have some ridiculous mega-whopper home plan for whatever reason). It usually has significantly lower download speeds (most businesses don't stream and download large files like home users). However, you do usually get better upload speeds.
2. It's a security issue. Spam emails often come from home setups by shady individuals who wear grey hoods all of the time, and businesses need to send emails, which is why these ports are open on busniness internet plans and not residential plans.