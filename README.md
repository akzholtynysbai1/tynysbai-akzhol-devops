# tynysbai-akzhol-devops

DevOps Laboratory Work 1 — Linux, Git, Docker and Jenkins.

| Field      | Value    |
|------------|----------|
| Name       | Akzhol   |
| Surname    | Tynysbai |
| Group      | IT2-2306 |
| Student ID | 38313    |
| Course     | DevOps   |

## Structure
```
app/app.py                          Python application (prints student info, HTTP on 8080)
scripts/Tynysbai_Akzhol_system.sh   Linux system information script
scripts/test.sh                     Project checks used by Jenkins "Test" stage
config/app.conf                     Application configuration
Tynysbai_Akzhol_info.txt            Student information
Dockerfile, docker-compose.yml      Docker configuration
Jenkinsfile                         CI pipeline: Checkout → Build → Test → Docker Build → Docker Run
```

## Run
```bash
./scripts/Tynysbai_Akzhol_system.sh
docker build -t tynysbai-akzhol-devops .
docker run -d -p 5000:8080 --name tynysbai-akzhol-container tynysbai-akzhol-devops
curl http://localhost:5000
docker compose up -d && docker compose down
```
