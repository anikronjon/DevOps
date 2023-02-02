## GIT

Install git on your local environment
- Download git from 
- Run the exe file

### Config your global settings
```docker
# Set Name and Email for all repository using --global
git config --global user.name "user_name"
git config --global user.email useremail@gmail.com
```

### Create a local git repository
```docker
# initialize git repository
git init
```

### Add a new file to the repo
```docker
touch new_file.txt
```

### Add the file to the staging environment
```docker
# For single file
git add new_file.txt
# or all file
git add .
# or only for txt file
git add *.txt
```

### Create a commit
```docker
git commit -am "commit name"
```

### Create a new branch
```docker
# To create new branch
git branch newbranch

# Go to this branch
git checkout newbranch
# or
git switch newbranch

# or (create and get inside of new branch -in one command)
git checkout -b newbranch

```

### Go to main/master branch
```docker
# checkout freture branch to main/master branch
git checkout master
# or 
git switch master
```