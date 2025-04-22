## LAB-1 GIT COMMANDS


### git clone https://github.com/AbhinavGiri21/devops.git

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/d29f93d81e1349b4356c69ac2f2ba2c24ddffd8b/500110031/image.png)

<pre>
git add . 
git commit -m "figure 1" 
git push 
</pre>

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/07eec930d5c786ba4d59ec44ccd7d9f7ea334c53/500110031/Screenshot%202025-04-08%20105125.png)

<pre>
git status
</pre>

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/2cd9edc5788a0b8ac8f79c637509abd35d05ff1c/500110031/Screenshot%202025-04-08%20105519.png)

## LAB-2 GIT COMMANDS
### BRANCHING
### Create a file and do 3 commits in it 1st change

<pre>
git add .
git commit -m "version1"
</pre>
### 2nd Change

<pre>
git add .
git commit -m "version2"
</pre>
### 3rd Change

<pre>
git add .
git commit -m "version3"
</pre>

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/3fd1d9f9856d8b07e8743ec98435109aa49c3031/500110031/Screenshot%202025-04-08%20110101.png)

### View all commits by using git log

<pre>
git log
</pre>

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/72c2390f65dc3864bc08f4b4804bf8a0131471ef/500110031/Screenshot%202025-04-08%20110320.png)

## GIT SUBMODULE

### CREATE THREE REPO IN GITHUB AND CLONE IT TO YOUR PC REPO1:MAIN-add index.html file->add->commit->push REPO2:CSS-add style.css file->add->commit->push REPO3:JS-add script.js file->add->commit->push

### open integrated terminal of MAIN repo

![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/eb85a436eea1eea1b248ac3390424eca44426e6c/500110031/Screenshot%202025-04-08%20110921.png)
![Alt text](https://github.com/user-attachments/assets/0067e257-108f-474a-bb90-3ee770af88b2)

## DOCKER

<pre>
  docker -v
</pre>
<pre>
  docker pull hello-world
</pre>
<pre>
  docker images
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/14d85579e47b69497b6bff9b58ac486408f786ac/500110031/Screenshot%20from%202025-04-22%2009-11-14.png)
<pre>
  docker run hello-world
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/0e64d05d3c8bb0f2928fd450a51b17a009a82bb8/500110031/Screenshot%20from%202025-04-22%2009-16-45.png)
<pre>
  docker run -it ubuntu
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/9314353ff7570d8e12caff9afd75fa442f06399a/500110031/Screenshot%20from%202025-04-22%2009-18-33.png)

<pre>
  docker ps -a
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/e2cbd5fe320ec268cbe6e343b99e245c0c6a3bc1/500110031/Screenshot%20from%202025-04-22%2009-22-21.png)

<pre>
 docker ps -a
 docker start youthful_yonath
 docker ps
 docker stop b8fe5708c23b
 docker ps
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/aafed02e6e5d3885970c41d3516eec9268b74c6a/500110031/Screenshot%20from%202025-04-22%2009-28-28.png)

## FastAPI Application with Docker Containerization

<pre>
  Purpose:

  Created a simple FastAPI app with two routes:

  /: Returns name and location.

  /{data}: Returns a custom "hi" message with the given data and location.

  Used uvicorn to run the FastAPI app on port 80 with auto-reloading enabled.
</pre>

<pre>
  from fastapi import FastAPI
  import uvicorn

  app = FastAPI()

  @app.get("/")
  def read_root():
      return {"name": "Sagar", "Location": "Dehradun"}

  @app.get("/{data}")
  def read_data(data: str):
      return {"hi": data, "Location": "Dehradun"}

  if __name__ == "__main__":
      uvicorn.run("main:app", host="0.0.0.0", port=80, reload=True)
</pre>

<pre>
from fastapi import FastAPI
import uvicorn

app = FastAPI()

@app.get("/")
def read_root():
    return {"name": "Sagar", "Location": "Dehradun"}

@app.get("/{data}")
def read_data(data: str):
    return {"hi": data, "Location": "Dehradun"}

if __name__ == "__main__":
    uvicorn.run("main:app", host="0.0.0.0", port=80, reload=True)
</pre>
![Alt text](https://github.com/AbhinavGiri21/DevOpsLabFSAI-B3/blob/4304b59872970d4dec54a037d659ddee93a551d9/500110031/Screenshot%20from%202025-04-22%2009-46-41.png)

## Automation Using GitHub Actions
<pre>
Aim:
To automate build and deployment workflows using GitHub Actions.
  
Tools/Technologies Used:
GitHub Actions, Docker
  
Procedure:
1.	Created a .github/workflows directory.
2.	Wrote a YAML workflow file to trigger Docker build on code push.
3.	Configured build and test jobs inside the workflow.
4.	Pushed changes to GitHub and observed automatic pipeline execution.
  
Output:
Automatic building of Docker image through GitHub Actions pipeline.
Learning/Conclusion:
Learned about CI/CD automation with GitHub Actions, reducing manual deployment efforts.
</pre>

## Jenkins Pipeline Integration

<pre>
Aim:
To automate project build and deployment using Jenkins integrated with GitHub.
  
Tools/Technologies Used:
Jenkins, GitHub
  
Procedure:
1.	Installed Jenkins on local server.
2.	Configured GitHub webhook for Jenkins project.
3.	Created a Jenkins pipeline job pulling from GitHub.
4.	Triggered build automatically on GitHub push.
5.	Deployed built project after pipeline success.
  
Output:
Successful automated build and deployment using Jenkins pipelines.
Learning/Conclusion:
Learned about continuous integration and delivery (CI/CD) concepts using Jenkins and GitHub together.
</pre>
