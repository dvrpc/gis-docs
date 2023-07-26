# GIS Enterprise Documentation
This repo is for documenting DVRPC's Enterprise GIS.

## Contributing
All are encouraged to develop and contribute new materials and recommend improvements to the existing guides. Any changes or new contributions will need be to be approved by the GIS team before inclusion in the published the docs. 

#### 1. Clone the repo
``` cmd
git clone https://github.com/dvrpc/gis-docs.git
```
#### 2. Create a branch
Before contributing you will need to create a new branch from `main`. Name it based on the feature/topic of the materials you are developing. 

#### 3. Create a Python virtual environment with dependencies
Working in the repo directory from your terminal:

create new venv
```cmd
python -m venv venv
```
activate venv
```
.\venv\scripts\activate
```
install requirements
```
pip install -r requirements.txt
```
#### 4. Start development server of mkdocs project
```
mkdocs serve
```
Open `http://127.0.0.1:8000/intro` in your browser to preview

Reference the Material for MkDocs Documentation for reference on project configuration and specific markdown features.

#### 5. Submit Pull Request with proposed changes
When you have completed the proposed changes create a PR to `main` branch to be reviewed by the team.