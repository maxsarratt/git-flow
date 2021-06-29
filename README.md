# Git Flow

**Description**

- General development will have two main branches: master (main) and develop. Main is the online version used by customers and cannot be changed at will. And develop is similar to the alpha version, which is tested by internal personnel. It will be merged into main if there is no problem
- Local refers to your own computer, and remote refers to the place where the code is placed on the Internet (Github, Bitbucket)

**Process**

Switch to the development branch before developing new features: `git checkout develop`

1. Local: Development branch
    - Synchronize the content of local and remote branches: `git pull` (similar to synchronizing cloud drives)
    - Open a new branch: `git checkout -b <Docking 7-11 Super Fetching Service>` (to avoid developing multiple functions at the same time and creates confusion)
2. Local: new branch
    - Develop new features
    - View branch file modification status: `git status`
    - Add changes to the cache: `git add .`
    - Confirm the modification and give a summary: `git commit -m "Complete the docking 7-11 super fetching service"`
    - Synchronize the content of local and remote branches: `git push` or `git push --set-upstream origin xxx`
3. Remote: Github.com
    - Open a Pull Request (PR) to merge the new branch into the development branch
    - Colleagues view and give feedback
    - Merge into development branch
4. Local: new branch
    - Switch to the development branch: `git checkout develop`
    - Go back to step 1
