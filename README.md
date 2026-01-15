
# GitTutorial
**This repository** has the finality to show :

- How config your GitHub account

- How Config SSH keys and hhtps for Git

- How Use Git Terminal

- How Config Git Terminal



## Prerequisites 🔧  
**To use Git and GitHub**, you must have already created a GitHub account.  
If you don’t, you can follow this tutorial:

- **Step 1**: Go to [GitHub](https://github.com)

- **Step 2**: Click on [Sign up](https://github.com/signup)

- **Step 2.1**: Complete the registration process and click on **Continue**

*Following these steps, you have successfully created your GitHub account!*

## 🧑‍💻 Configuring Git Username and Email (Local Identity)

Before making commits, you need to tell Git who you are. This is important so that your commits are properly labeled.

### 1. Set your Git username:
```bash
git config --global user.name "Your Name"
```

### 2. Set your Git email:
```bash
git config --global user.email "your_email@example.com"
```

### 3. Check your configuration:
```bash
git config --global --list
```

You should see something like:
```
user.name=Your Name
user.email=your_email@example.com
```

## GitHub SSH Key 🔐

To connect your local Git environment to GitHub securely, you can use either HTTPS or SSH. SSH is often preferred for its security and ease once set up.

### 🔑 SSH Method (Recommended)

 - **Check for existing SSH keys**  
   
   Open your git terminal and run:
   ```bash
   ls -al ~/.ssh
   ```
   If you see files like `id_rsa.pub`, you already have an SSH key. 

 - **Generate a new SSH key**
   
   If is your first using git run this  :
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
    *Also You can use a GitHub email address to keep your personal email private.*

- **Add the SSH key to the ssh-agent**
   ```bash
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_ed25519
   ```

- **Add the SSH key to your GitHub account**
   - Copy the key to your clipboard:
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
     Then copy the output.

   - Go to your GitHub profile and enter to :

        ***Settings** > **SSH and GPG Keys** > **New SSH Key**  .*
     
     Paste the copied key, add a title, and save.

    - Test your SSH connection :

        ```bash
        ssh -T git@github.com
        ``` 
        **If is successfully you should see a message like**
        ```bash
        Hi your-username! You've successfully authenticated.
         ```
        



## Congratulations you can use Git and Github as GOD
Dont forget to enter to folder exercise to practice and improve your dev skills :D
    




