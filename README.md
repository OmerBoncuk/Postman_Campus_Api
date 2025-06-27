# API Test Environment User Stories

This project contains user stories and acceptance criteria prepared for an API test environment.  
It covers test scenarios for multiple microservices and prioritized business requirements.

## 📌 Project Purpose

- To perform CRUD operations over API
- To manage entities such as State, City, and Course
- To ensure the system responds within the specified performance times
- To validate required checks during user exam creation processes

## 🚀 User Stories

| ID    | Priority | User Story |
|-------|----------|------------|
| US001 | M        | As a user, I want to log in to the test environment via the API so that I can perform authorized operations. |
| US002 | M        | As a user, I want to add and query states in the system via the API. |
| US003 | M        | As a user, I want to perform CRUD operations for a state (States) via the API. |
| US004 | M        | As a user, I want to perform CRUD operations for a city (City) via the API. |
| US005 | M        | As a user, I want to ensure necessary validations for a course over the API. |

_(For more user stories, please refer to the Excel file.)_

## ✅ Sample Acceptance Criteria

- **US001 - API Login**  
  - AC001: When attempting to log in with an invalid username or password, it should return `401 Unauthorized`.

- **US002 - Add State**  
  - AC002: If the country does not have the state in the request body, it should return `400 Bad Request`.

- **US003 - List States**  
  - AC101: The list of all states should be returned in under 1000 ms.

_(For all acceptance criteria, please see the source file.)_

## 👥 Team Members

| Member | Role |
|-----------|----------------|
| 🧑‍💻 [Erdem Özkan](https://github.com/ErdemOzkann) | QA |
| 👩‍💻 [Diyar Ölmez](https://github.com/diyar-olmez) | QA |
| 👨‍💻 [Barış Saydam](https://github.com/BarisSaydam) | QA |
| 👨‍💻 [Ömer Boncuk](https://github.com/OmerBoncuk) | QA |
| 👨‍💻 [Atilla Toros Avcı](https://github.com/AtillaTorosAvci) | QA |
| 👩‍💻 [Gamze Batmaz](https://github.com/GAMZE3845) | QA |

> Team coordination was conducted via RocketChat.  
> Work was divided into Cucumber scenarios based on individual responsibilities.

## 🛠 Installation & Usage

```bash
# Clone the project
git clone https://github.com/username/project_name.git
cd project_name

# (If applicable) install dependencies
npm install
# or
pip install -r requirements.txt

# Start the project
npm start
# or
python main.py
