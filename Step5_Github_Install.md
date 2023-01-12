# Tutorial: Github

<img width="276" alt="image" src="https://foundations.projectpythia.org/_images/GitHub-logo.png">

### Github
#### What is Github
- Github is a code hosting platform for version control and collaboration
- Github allows you to work together on code with people from around the world
- Github has excellent version control of all submited code 
#### Why use Github?
- Github allows for easy collobaration across multiple people
- Github version control allows you to save yourself when you break your code or your computer 😅 
- Github repos are a great display of your past work and coding skills for future employers

### Create a Github & Install Github Desktop
1. Sign up for github: https://github.com/signup?user_email=&source=form-home-signup
2. Install Github desktop: https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop?platform=windows


### Create your first Repositry (Repo)

<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211663921-c5c6d7b0-3f6c-40ca-af67-453b35c733f6.png">

<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211666184-9a13d6fd-0c4b-4387-9f6c-31bde97b21ad.png">

<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211666820-c76a80ab-2d57-434b-92de-5e6953cdb090.png">

<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211667059-2af7c718-bccd-4ccd-aa65-4c520cb15a60.png">

<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211667252-557bc8e2-8f13-414d-a4f2-5c2c33b32bad.png">


### Add and push a file to Github

1. Open your terminal and go into the folder of your repo. This is where you saved it in the step right above.
  - Reminder: `cd` changes directories and allows you to move around, `pwd` allows you to see where you are in the command line
2. Check your README.md was created by using `ls` and seeing if it appears
3. Create a new file using touch
```bash
touch new_file.txt
```
4. Reopen Github Desktop, there should now be a new file there called new_file.txt
<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211669058-17275336-77ac-4399-a21e-f056523f2e78.png">
5. Add a Name and Description for the commit, then click 'commit to main'
<img width="600" alt="image" src="https://user-images.githubusercontent.com/25289269/211669263-9b1ad4c8-23b4-4f42-ba37-9db2e0b4c5c9.png">
6. Press 'Push orgin' in the corner to push your changes from your local computer to Github.com
<img width="289" alt="image" src="https://user-images.githubusercontent.com/25289269/211669528-b30d01e3-6365-468e-9dbf-7252b9c1f296.png">
7. Go back to https://github.com and see your most recent commit 🎉
<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/211670127-e1859b36-0fd4-42da-a992-4d649e2fd733.png">

### Install command line version of Git

1. Use this guide to install: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
2. Test to see that you installed github correctly by typing the following into your command line
```bash
git --version
```

### Clone a repo from Github using command line

1. Find the repo you want to clone, we will be using: https://github.com/MED263-WI23/MED263_Intro , and copy the link
<img width="750" alt="image" src="https://user-images.githubusercontent.com/25289269/212199877-748ca742-ac90-40e1-86c9-a9f2862a74fa.png">
- Make sure you are have 'HTTPS' highlighted in the Clone Window on Github

2. Open up a command line and navigate to where you want to save this repo, then clone the repo

```bash
git clone https://github.com/MED263-WI23/MED263_Intro.git
```

3. There should now be a new folder titled **MED263_Intro** which contains all the code from the repo!





