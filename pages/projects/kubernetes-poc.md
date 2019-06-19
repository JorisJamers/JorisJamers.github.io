# Kubernetes - Proof of Concept

Together with XTi and Refleqt we created a Kubernetes POC. This project was a research project on how we could create the best workflow for new projects using Kubernetes.

This project was a mix of some skills I got from the Descours & Cabaud project and the Private GKE cluster project. This combined Kubernetes with Gitlab and Maven.

Instead of using Jenkins for the CICD we used Gitlab. The use of Gitlab made me learn some new Terraform skills as well, how we could provide Gitlab environment variables on a group level instead of manually provide them in the projects. And the way I saw Terraform in a pipeline. Using some Gitops I started putting my Terraform code in Gitlab so that developers could destroy or create DEV environments with only a value change on a variable. To test this I also wrote some python code to refresh my python skillset.

[Back](../projects.md)

[Home](../../index.md)
