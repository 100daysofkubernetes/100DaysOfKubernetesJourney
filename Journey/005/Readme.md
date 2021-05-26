# KubeCon Day 1 and Using Visual Code with GitHub and getting verified commits to GitHub

## Introduction
Today was the first day of KubeCon. And I also figured out how to ensure I have verified badge on my GitHub Commits when I push using Visual Code.

## Research

A reference I keep coming back to > [kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
[Cisco - Kubei : A Kubernetes Runtime Vulnerabilities Scanner](https://www.ciscotechblog.com/blog/kubernetes-runtime-vulnerabilities-scanner-launch/?ccid=cc002449)
[Cisco - Mitre ATT&CK framework: What is it and does it work for K8s environment? ](https://www.ciscotechblog.com/blog/mitre-attck-framework-what-is-it-and-does-it-work-for-k8s-environment/?ccid=cc002449)

From KubeCon Europe, I covered:
- Keynote
- Introduction and Deep Dive Into Containerd - Kohei Tokunaga & Akihiro Suda, NTT Corporation
- Secrets Store CSI Driver: Keeping Secrets Secret - Anish Ramasekar, Microsoft & Tommy Murphy, Google
- Lessons Learned from Operating ETCD - Pierre Zemb, OVHcloud
- Writing for Developers: Take your Project Docs to the Next Level - Celeste Horgan, CNCF
- Ask Me Anything with Joe Beda, Co-creator of Kubernetes (I actually missed this one)

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

For getting the verified badge on my commits, [I wrote this blog post](https://veducate.co.uk/github-verified-code/)