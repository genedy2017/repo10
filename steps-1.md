# Local Repo

1. Install git: [Git website](https://git-scm.com)
2. git bash
3. Configure git:

    ```
    git config --global user.name "Samir Aly"
    git config --global user.email "samir@gmail.com"
    git config --global core.editor /path/to/editor
    ```

4. `mkdir repo10`
5. `cd repo10`
6. `git init`
7. `touch index.html`
8. `edit and save file`
9. `git add index.html`
10. `git commit -m "Add new index file"`
11. `git log`
12. `git log --stat`
13. `git log --pretty=oneline`
14. `git log -n 4`
15. To stage and commit in one step:
    `git commit -a -m "Message"`
16. `git show a59z`
17. `git diff a59z b3eer`
18. `git checkout a59z`
19. `git checkout master`

---

# Preparing a remote repo on github:
    
1. create new repo on github
2. create ssh key pair (public + private)
    https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
    `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
3. upload public key to github
    `cat ~/.ssh/keyname.pub`
4. define private key to local repo
    `eval $(ssh-agent -s)`
    `ssh-add ~/.ssh/keyname`
5. Define remote repo:
    `git remote add origin git@github.com:username/repo-name.git`
6. `git push -u origin master`