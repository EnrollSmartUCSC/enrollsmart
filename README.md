# Enroll Smart
## description
Enroll Smart is a simple solution to enrollment problems at UCSC. Students can use it as a one‐stop solution to enrollment problems where they can plan their degree, check the requirements on the course catalog, check offerings of classes, and read reviews by previous students. During peak enrollment season, students can even sign up for updates about open spots in high‐demand classes. We aim to unify different locations to search in one place to make enrolling into your class faster and easier.
## features
- Check the description and prerequisites of a course.
- Pin courses you have a keen interest in.
- Schedule courses by quarter to plan your degree by **dragging and dropping**.
- Add a course to the watchlist for a particular quarter.
- Track the status of classes and get notified of updates and available positions in the course.

## Architecture
### Backend
#### dependencies and requirements
All the dependencies stated below can be installed by running the following commands in `/backend`
```bash
# if python venv not created
python3 venv <venv_name>
# ---------------------------------
source <venv_name>/bin/activate
pip3 install -r ./requirements.txt
```
- Flask
- flask-cors
- firebase-admin
- requests
- psycopg2
- python-dotenv
- flasgger
- beautifulsoup4
- regex
#### hosting
The backend is hosted on an AWS EC2 instance, while the database is hosted on AWS RDS as a PostgreSQL instance.
### Frontend
#### dependencies and requirements
-  @dnd-kit/core
-  @emotion/react
-  @emotion/styled
-  @mui/icons-material
-  @mui/material
-  @radix-ui/react-scroll-area
-  @radix-ui/react-select
-  @radix-ui/react-slot
-  @radix-ui/react-switch
-  @radix-ui/react-tabs
-  antd
-  class-variance-authority
-  clsx
-  firebase
-  lucide-react
-  next
-  next-auth
-  react
-  react-dom
-  tailwind-merge
#### hosting
Hosting is done on AWS Amplify by Domain name by https://name.com
