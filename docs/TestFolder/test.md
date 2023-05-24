---
sidebar_position: 1
---

# Configure multiple SSH for github

If you wanna configure SSH for different accounts, please read follow contents:

## 1. Create your first React Page

Generate 2 pairs of ssh-keys:

```jsx title="src/pages/my-react-page.js"
ssh-keygen -t rsa -f "customize name"
```

Then you get id_rsa and id_rsa.pub

## 2. Configure ssh in your github

Add ~.pub file in your github settings

## 3. Create or update your config file in .ssh folder

Create a config file if you don't have it in .ssh folder

```
# key1 one github account
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id-rsa

# key2 another github account
Host me.github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/jiaxi

```