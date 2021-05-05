# New post title here

## Introduction


## Prerequisite


## Use Case


## Research

Issues with Visual Code pushing to my repo: 
> > git push origin main:main
> remote: error: GH007: Your push would publish a private email address.        
> remote: You can make your email public or disable this protection by visiting:        
> remote: http://github.com/settings/emails        

[Fixed with the following](https://github.community/t/push-declined-due-to-email-privacy-restrictions/990/5) in the terminal of Code where I had the push issue:
> CMD: git config --global user.email “YOUR_EMAIL_ADDRESS_HERE@users.noreply.github.com”
> CMD: git commit --amend --reset-author
> CMD: git push

Maybe better instructions on [Stack Overflow here](https://stackoverflow.com/a/51097104)
## Try yourself
