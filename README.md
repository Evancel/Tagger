# Tagger
git project to work with tags
link to my Notion: https://www.notion.so/Git-project-Tagger-130f96cc224a808fa109cea245a2b91c
link to HyperSkills: https://hyperskill.org/projects/377

git init
git remote add origin file:///tmp/tagger

echo -e "from datetime import datetime

def get_day_name():
date_obj = datetime.utcnow()
day_name = date_obj.strftime('%A')
return day_name" >> [main.py](http://main.py/)
git add .
git commit -m "feat: Day name function"

git tag v0
git push --set-upstream origin main
git push --tags

git tag -d v0
git push origin --delete v0
git tag -a 0.1.0 -m "Day name functionality"
git push --tags

echo -e "from datetime import datetime

def get_day_name():
date_obj = datetime.utcnow()
day_name = date_obj.strftime('%A')
return day_name

def get_month_name():
date_obj = datetime.utcnow()
month_name = date_obj.strftime('%m')
return month_name" > [main.py](http://main.py/)
git add .
git commit -m "feat: Month names"
git tag -a 0.2.0 -m "Month name functionality"
git push origin main --tags

echo -e "from datetime import datetime

def get_day_name():
date_obj = datetime.utcnow()
day_name = date_obj.strftime('%A')
return day_name

def get_month_name():
date_obj = datetime.utcnow()
month_name = date_obj.strftime('%B')
return month_name" > [main.py](http://main.py/)
git add [main.py](http://main.py/)
git commit -m "fix: Bug fix month name"
git tag -a 0.2.1 -m "Month name bug fix"
git push origin main 0.2.1

git tag -l -n
