### Spring Boot Application - AWS CI/CD Deployment Pipeline Project

This project demonstrates the creation of a fully automated deployment pipeline for a Docker containerized Spring Boot application using AWS services. It integrates AWS CodeBuild, AWS CodeDeploy, and AWS CodePipeline for continuous integration and continuous deployment (CI/CD). Additionally, it incorporates Amazon Simple Notification Service (SNS) and Amazon Simple Queue Service (SQS) to provide real-time deployment status notifications.


![1698210690862](https://github.com/nusairc/AWS-CICD-Project/assets/98309865/4b3914de-8277-4b8b-b5a9-e58fdc64fd11)

## Important Note

While you're welcome to explore and use the files and code provided, I strongly encourage you to understand the concepts behind it.
Cloning the repo without understanding its workings may limit your ability to adapt and troubleshoot in different contexts. Take the time to explore the documentation of AWS DevOps Tools , AWS ECS , AWS ECR , AWS SQS & SNS. Experiment with different configurations, make changes, and observe the effects. AWS CI-CD is a powerful approach, and it's essential to grasp the fundamentals before applying it to real-world scenarios

Project Steps

Step 1: Code Setup ,
In this initial step, we set up the foundation for the project:

    Created a GitHub repository to host the source code.
    Generated a Spring Boot project using Spring Initializer.
    Integrated a Dockerfile into the project for containerization.
    Pushed the entire codebase to the GitHub repository.

Step 2: Configuring Code Build and Deployment

This step focuses on configuring the CI/CD pipeline:

    Configured AWS CodeBuild to use the GitHub repository as the source (using GitHub Connection).
    Created an Amazon Elastic Container Registry (ECR) repository.
    Prepared the application code as a Docker container image.
    Employed a buildspec.yaml file in the repository to define the build process, including pushing the Docker image to Amazon ECR.
    Set up AWS CodeDeploy to use the Docker image from Amazon ECR for deploying the application into Amazon Elastic Container Service (ECS).
    Ensure that an IAM service role is created for CodeBuild to access ECR.

Step 3: Setting Up ECS and Related Services

In this step, we configure Amazon ECS and its associated services:

    Created an Amazon ECS cluster to host the application.
    Defined an ECS task definition that specifies the application's requirements and resources.
    Created an ECS service using the task definition to manage the application's desired state.
    Configured the necessary security groups for access and communication.

Step 4: Creating a Code Pipeline

This step involves creating an AWS CodePipeline to automate the deployment process whenever changes are pushed to the GitHub repository. A continuous delivery pipeline ensures that the application is deployed efficiently and reliably.

Watch the video tutorial given below for a detailed walkthrough of this step.
Step 5: Configuring SNS & SQS for Notifications

Real-time notifications about deployment statuses are essential for monitoring and troubleshooting. In this step, we set up SNS and SQS for notifications:

    Created an Amazon SNS topic to handle notifications.
    Established an Amazon SQS queue to receive notifications.
    Subscribed the SQS queue to the SNS topic, allowing it to receive messages.
    Configured the CodePipeline to send SNS notifications on deployment status changes, ensuring that you are promptly informed of any updates or issues in the pipeline.

This project provides a comprehensive example of setting up a robust CI/CD pipeline for a Spring Boot application on AWS. For a more detailed guide and visual walkthrough, refer to the [video tutorial I have refered .](https://youtu.be/ARGmrYFfv44?si=R25lEtDO-CUrN4TB)

## Cleaning Up

Remember to stop or terminate your AWS resources after use to avoid unnecessary charges. 

Feel free to clone this repository as a foundation for your own projects. Just make sure to update the AWS repository name and account ID to match your AWS environment. for any queries related to project reach me on nusairtech@gmail.com or www.linkedin.com/in/nusair 

