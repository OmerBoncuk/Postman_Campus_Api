# 📚 Campus API - Automated API Testing with Postman

This repository contains **Postman-based** automated tests for the **Campus API** (`https://test.mersys.io`).  
The goal is to validate API endpoint functionality and catch regressions or integration issues quickly.

---

## 🚀 Technologies Used

- **Postman** – for creating test scenarios and managing collections  
- **Postman Test Scripts** – for JavaScript-based assertions  
- **Newman** – CLI tool for running collections (great for CI/CD)  
- **JSON Environment** – for managing tokens and dynamic environment data  

---

## ⚙️ Environment & Security

- **Base URL:** `https://test.mersys.io`
- **API Base Path:** `/school-service/api/{...}`
- **Content-Type:** `application/json`
- **Admin Credentials:**
  - **Username:** `turkeyts`
  - **Password:** `TechnoStudy123`

Authentication is done by sending a request to `/auth/login` and using the returned token in the header of subsequent requests.

---

## 📊 Test Summary Table
| ID        | User Story Description             | Endpoint(s)                            | Expected Status Codes            | Notes                                             |
| --------- | ---------------------------------- | -------------------------------------- | -------------------------------- | ------------------------------------------------- |
| **US001** | Login to API to obtain admin token | `/auth/login`                          | `200` (success), `400` (invalid) | Tests login with valid & invalid credentials      |
| **US002** | Add a country with a state         | `/countries`                           | `201`                            | Verifies country, code, and state details         |
| **US003** | CRUD operations on states          | `/states`                              | `200`, `201`, `204`              | Includes list (<1000ms), add, edit, delete        |
| **US004** | CRUD operations on cities          | `/cities`                              | `200`, `201`, `204`              | List all <1000ms, specific city <200ms            |
| **US005** | CRUD operations on exams           | `/exams`                               | `200`, `201`, `400`, `404`       | Checks creation, update, deletion, validation     |
| **US006** | CRUD on custom fields              | `/custom-field-groups`                 | `200`, `201`, `400`, `204`       | Prevents duplicate `name` or `orderNo`            |
| **US007** | CRUD on student groups             | `/student-group`                       | `200`, `201`, `400`              | Includes validations on name & description length |
| **US008** | Add students to groups             | `/student-groups/{id}/add-students`    | `200`                            | Verify by listing students in group               |
| **US009** | Remove students from groups        | `/student-groups/{id}/remove-students` | `200`                            | Ensure students are removed from group            |
| **US010** | CRUD on education standards        | `/education-standard`                  | `200`, `201`, `204`, `400`       | Lists standards by school ID                      |
| **US011** | CRUD on grading schemes            | `/grading-schemes`                     | `200`, `201`, `204`, `400`       | Validates name, type, and school link             |
| **US012** | CRUD on incident types             | `/incident-type`                       | `200`, `201`, `204`, `400`       | Ensures proper incident data & error handling     |


CampusAPI_Postman/
├── CampusAPI.postman_collection.json
├── CampusAPI_ENV.postman_environment.json
└── README.md



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
