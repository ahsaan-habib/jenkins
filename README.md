# Jenkins Docker Setup

This repository provides a Docker Compose configuration for running Jenkins in a Docker container. It allows you to quickly set up and run Jenkins on your local machine or a dedicated server.

## Prerequisites

Before getting started, ensure that you have the following prerequisites installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

To set up Jenkins using Docker, follow these steps:

1.  Clone this repository to your local machine or server:

        git clone https://github.com/your-username/jenkins-docker.git

2.  Navigate to the cloned repository:

        cd jenkins-docker

3.  Customize the `docker-compose.yaml` file if needed. You can modify the Jenkins container's ports, volumes, or any other configurations according to your requirements.

4.  Start the Jenkins container:

        docker-compose up -d

This command will download the Jenkins image and start a new container based on the provided configuration.

5. Access Jenkins in your web browser:

Open your preferred web browser and visit [http://localhost:8080](http://localhost:8080) (if running locally) or replace `localhost` with the IP address or domain name of your server.

6.  Follow the on-screen instructions to complete the Jenkins setup process. Retrieve the initial administrator password from the Jenkins container logs by running the following command:

        docker logs jenkins

Copy the generated password and paste it into the Jenkins setup wizard.

7. Install any desired plugins and configure Jenkins according to your requirements.

## Usage

Once Jenkins is set up and running, you can start creating and running your build jobs, pipelines, and perform other CI/CD tasks using the Jenkins web interface.

To stop the Jenkins container, run the following command:

## Contributing

If you have any suggestions, improvements, or issues, please feel free to open an issue or submit a pull request. Contributions are welcome!

## License

This project is licensed under the [MIT License](LICENSE).

### get admin password

        docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
