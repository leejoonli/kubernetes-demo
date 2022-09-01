# Project Description

Repository to track a walkthrough of Kubernetes.  This will be a folder of YAML files that are meant to be used with Kubernetes.

# Technologies Used

- Kubernetes
- Minikube
- Kubectl

> There's a possibility of you needing to install Docker as well.  For more information on installing Docker visit https://docs.docker.com/get-docker/.

> Information on installing Minikube can be found here: https://minikube.sigs.k8s.io/docs/start/.

> Information on installing Kubectl can be found here: https://kubernetes.io/docs/tasks/tools/.

# Installation

> You must have Minikube and Kubectl installed.

1. Open your terminal and navigate to your desired directory where you want to store this repository using `cd <YOUR DIRECTORY HERE>`.
2. On this GitHub repository, click on the "Code" dropdown menu and either click on "HTTPS" or "SSH" depending on what you're using.
    * You can either click the link which will highlight the GitHub or HTTPS link and copy it or click on the icon next to the link which will copy it into your clipboard.
3. Clone this repository to your machine using the `git clone <PAST SSH OR HTTPS HERE>` command.
4. `cd` into the newly created directory.
5. Start Minikube with `minikube start`.
6. You will need to apply the YAML files by running the following commands:
    * `kubectl apply -f mongo-configmap.yaml`.
    * `kubectl apply -f mongo-secret.yaml`.
    * `kubectl apply -f mongo.yaml`.
    * `kubectl apply -f mongo-express.yaml`.
    > The `dashboard-ingress.yaml` file is used only if Ingress is installed.  This is not necessary and does require knowing how to edit hosts file.
7. Run the application using `minikube service mongo-express-service`.
    > Your browser should open or a new tab should open.