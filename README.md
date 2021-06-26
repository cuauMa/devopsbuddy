# devopsbuddy
## Fullstack AWS Trainning - Udemy trainning from Marco Tadone

## How to build
Rund the following commnad:
```sh
mvn clean install
```

## Centralized Workflow
```sh
git status
vi README.md
git add .
git commit -m "Initial creation"
git push
```

## Branched Workflow
- User 1 - Create the feature1
```sh
  553  git checkout -b feature1
  555  echo "feature1 content" > feature1.txt
  559  git add .
  560  git commit -m "feature1 added"
  563  git push -u origin feature1

  565  git checkout master
  566  git pull
  567  git merge feature1 
  568  git push
```

## Git-Workflow Branched Workflow
- User 2 - Create the feature2
```sh
  569  git checkout -b develop
  570  git push -u origin develop

  571  git checkout -b feature2
  572  echo "Feature2 content" > feature2.txt
  573  git add .
  574  git commit -m "feature2.txt added"
  575  git push -u origin feature2

  576  git checkout develop
  577  git merge feature2
  578  git push

  579  git checkout master
  580  git pull
  581  git merge develop
  582  git push

  591  git tag -l
  592  git status
  593  git tag "1.0.0.RELEASE" -m "Releasing version 1.0.0"
  594  git push --tags
```

## SSH generated
- 1 Generate the ssh key
```sh
  383  ssh-keygen
  384  ssh-keygen -t ed25519 -C "t@hotmail.com"

  484  ssh-keygen -o
  486  clip < cuauma-github.pub 
```
- 2 Add the .ssh folder to the ssh agent
```sh
# NOT WORKING - SHOW A MESSAGE ERROR 
  507  eval ssh-agent
  508  ssh-add.exe ~/.ssh/cuauma

# NOT WORKING - SHOW A MESSAGE ERROR
  510  eval 'ssh-agent -s'
  511  ssh-add.exe ~/.ssh/cuauma

# THIS COMBINE COMMANDS ITS WORKS!!!! 
  527  eval $(ssh-agent)
  528  ssh-add.exe ~/.ssh/cuauma
```