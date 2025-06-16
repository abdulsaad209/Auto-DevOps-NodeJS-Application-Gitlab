## Prerequisites:
* A k8s cluster setup and integrated as gitlab-agent in GitLab
* MongoDB, If you dont have you can use the container image: saadzahid/solarsystem-mongodb:01
* 2 branches one is feature-1-testing and second is main branch

### Step1:
* Clone the repository and add in the GitLab project. It would be good if group and project name would be.
* Group: devops-group
* Project: Auto-DevOps-NodeJS-Application-Gitlab

### Step2:
* Store below variables in your GitLab CICD variables according to your values
![image](https://github.com/user-attachments/assets/8e3479c4-ca14-4da4-8554-19487388792a)
![image](https://github.com/user-attachments/assets/0450abbd-093d-49c4-9051-626f2bb7d6d9)
* Remember variables should be store in correct environment as shown in the images.

### Step3:
* Configure your gitlab Agent using variable KUBE_CONTEXT, If you dont want to use gitlab agent and wanna configure kube config content present in ~/.kube/config at k8s cluster.
* Then use **KUBECONFIG** instead of **KUBE_CONTEXT** in the variables. And store variable as file type.

### Step4:
* Push changes to feature-1-testing branch. And everything goes well then run stop review job manually.

### Step5:
* Create merge request and merge changes into main branch and it will deploy into production.

### Building and Deploying in Staging Environment
![image](https://github.com/user-attachments/assets/7e0a333e-20e0-46e3-9f3a-d713033fab08)

### Building and deploying in Production Environment
![image](https://github.com/user-attachments/assets/90cd3a8b-ce73-4704-9882-0a42d34a3e08)

### Production Environment
![image](https://github.com/user-attachments/assets/e981ef70-c38f-4d46-9ee9-996263c52c67)


### Deployed Application Interface
![image](https://github.com/user-attachments/assets/fae733be-08dd-47a1-b8b9-9bc3f9fb6e91)
