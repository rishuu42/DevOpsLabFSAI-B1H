# DevOps Lab 6 - Learning FastAPI and Docker

## Author
**Gurmehr Singh Gulati**  
**500101995**  
**R2142220078**  
**Full Stack AI B1-Hons**

---

## Overview
In this lab session, we learned how to set up **FastAPI**, create a basic API, and **dockerize** the application for deployment.

## Steps to Set Up FastAPI and Docker

### 1. Open WSL
```sh
wsl
```

### 2. Install Python
```sh
sudo apt install python3-pip -y
```

### 3. Install FastAPI and Uvicorn
```sh
pipenv install fastapi uvicorn
```

### 4. Open Visual Studio Code (through Ubuntu)
```sh
code .
```

### 5. Create a Project Directory and Necessary Files
#### `main.py`
```python
from fastapi import FastAPI
import uvicorn

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, World!", "status": "running"}

@app.get("/{data}")
def read_data(data: str):
    return {"input": data, "status": "received"}

if __name__ == "__main__":
    uvicorn.run("main:app", host="0.0.0.0", port=8080, reload=True)
```

#### `requirements.txt`
```
fastapi
uvicorn
```

#### `Dockerfile`
```dockerfile
FROM ubuntu

RUN apt update -y
RUN apt install python3 python3-pip pipenv -y

WORKDIR /app
COPY . /app/
RUN pipenv install -r requirements.txt

EXPOSE 8080 

CMD pipenv run uvicorn main:app --host 0.0.0.0 --port 8080 --reload
```

### 6. Build Docker Image
```sh
docker build -t fastapi-app .
```

### 7. Verify Docker Image Creation
```sh
docker images
```

### 8. Run the Docker Container
```sh
docker run -p 8080:8080 fastapi-app
```

---

## Key Learnings
- How to **set up FastAPI** and create a basic API.
- How to **write a Dockerfile** to containerize a FastAPI application.
- How to **build and run a Docker container**.
- How to **expose ports** and access the API from a web browser or API client.

---
<!-- ---

## Reference Repository:
[DevOpsLabFSAI-B1H](https://github.com/gurmehr04/DevOpsLabFSAI-B1H) -->
