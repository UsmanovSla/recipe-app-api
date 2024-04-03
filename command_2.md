<!-- Open VSCode in actual folder -->
cmd > code .

<!-- Build docker images via docker-compose -->
docker-compose build

<!-- Run docker with flake8 shell -->
docker-compose run --rm app sh -c "flake8"

<!-- Run docker with django: Start project -->
docker-compose run --rm app sh -c "django-admin startproject app ."

<!-- Run docker: Start new app -->
docker-compose run --rm app sh -c "python manage.py startapp core"

<!-- Run app (Django server) in docker container -->
docker-compose up
docker-compose -f docker-compose-deploy.yml up

<!-- Remove containers -->
docker-compose down
docker-compose -f docker-compose-deploy.yml down

<!-- Run docker with Test -->
docker-compose run --rm app sh -c "python manage.py test"


<!-- Run docker with Migrate models -->
docker-compose run --rm app sh -c "python manage.py makemigrations"
docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"

<!-- Run docker amd Create Superuser -->
docker-compose -f docker-compose-deploy.yml run --rm app sh -c "python manage.py createsuperuser"

<!-- Docker -->
 docker volume ls
 docker-compose down
 docker volume rm recipe-app-api_dev-db-data

<!-- Git -->
git add .
git commit -am "Update packages"
git push origin

<!-- SSH -->
cd C:\Users\usman/.ssh
ssh-keygen -t rsa -b 4096 -C "usm@recipe-app"
 + filename
 + passphrase
cat recipe_id_rsa.pub


<!-- git -->
cd Courses
git clone git@gitlab.com:maindev4/recipe-app-api-proxy.git

<!-- GitHub Course -->
git log
# 'q' - exit from log
git log --oneline


git config user.name
git config --global user.name "Tom Hulk"

git config user.email
git config --global user.email "Tom Hulk"

git status
git init

git add .
git add file1 file2
git rm --cached file1

git commit -m "My msg"

# add all + commit
git commit -a -m "My msg"

# commit with editor
git commit

# set VScode editor (default vim)
git config --global core.editor "code --wait"

git restore file1

# amend the commit: update previous commit
git commit --amend

# .gitignore
*.log
directory/
files.txt

# templates
gitignore.io
https://www.toptal.com/developers/gitignore/
https://www.toptal.com/developers/gitignore/api/python
https://www.toptal.com/developers/gitignore/api/django

# Branches
git branch
git branch new_branch
git switch new_branch

# delete branch (not head)
git branch -d new_branch

# force delete branch (not head)
git branch -D new_branch

# rename head branch
git branch -m new_name_branch

# create and switch to branch
git switch -c name_branch

# Checkout (as switch + other options)
git checkout name_branch

# Fastforward merge name_branch to master
git switch master
git merge name_branch

<!-- Terminal Win -->
# clear terminal
clear

# open directory in explorer
start .
start Directory

# list of directory
ls

# list of directory with hidden files
ls -a
ls Directory
ls Directory/Subdirectory

# actual path
pwd

# change directory
cd
cd ..
cd Directory/

# File creation
touch new_file.txt
touch first.txt second.txt third.txt

# File remove
rm new_file.txt

# directory creation
mkdir newdir

# Directory remove
rm -rf newdir
