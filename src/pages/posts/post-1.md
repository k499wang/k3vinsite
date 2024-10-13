---
layout: ../../layouts/Blog.astro
title: "My First DevOps Project"
date: "2024-10-13"
description: "The first post on his beginners DevOps project"
author: "Kevin"
---

# Introduction
This blog was a simple side project I took on to gain hands-on experience with DevOps. I chose to create a static website, which was an ideal beginner project. It allowed me to focus on the core principles of DevOps without getting bogged down in the complexities of app development.

Below is an outline of the general steps I followed to build this static site. Since it was my first time tackling something like this, I did encounter several challenges along the way.

The main repositories can be found here: 
- https://github.com/k499wang/iac-code/
- https://github.com/k499wang/k3vinsite

## Step 1: Domain Purchase
I started by purchasing a domain, which is now my site’s home: k3vinwvng.com.

## Step 2: Version Control with Git
Next, I got familiar with Git and created two repositories: one for my Infrastructure as Code (IaC) setup using Terraform and Ansible, and another for the static site’s source code.

## Step 3: Choosing a VPS Provider
I decided to use a Virtual Private Server (VPS) provider with strong Terraform support. Since I had previous experience with DigitalOcean and it offered free credits, I opted to stick with them.

## Step 4: Setting Up the VPS with Terraform
I automated the setup of my DigitalOcean droplet using Terraform. This included configuring DNS settings, managing SSH keys, and providing the necessary provider information to streamline the VPS setup.

## Step 5: Configuring the Server with Ansible
With the server up and running, I used Ansible to configure the necessary packages. Since I chose Astro for the static site framework, I needed to install Node.js and npm. This turned out to be more complicated than expected, as the default package manager provided an outdated Node.js version. To resolve this, I manually downloaded and installed the correct version via my Ansible playbook.

Additionally, I installed Nginx for web server management, configured it, and performed system cleanup. To keep the playbooks manageable, I broke them into roles and added tests to ensure everything was correctly installed.

## Step 6: Building and Deploying the Static Site
After setting up the infrastructure, I built my static site with Astro, made a few custom modifications, and learned some HTML and JavaScript in the process. I then uploaded the site’s code to GitHub.

Initially, I faced challenges with my GitHub Actions workflow. I manually built the files and copied them to /var/www/astro on my server, which wasn’t the most efficient solution.

## Step 7: Switching to GitHub Pages
Eventually, I discovered a simpler solution: GitHub Pages. I leveraged its built-in Actions to automate the deployment process. I also created two branches in my k3vinsite repository, showcasing my original manual deployment workflow alongside the more streamlined GitHub Pages setup.

## Conclusion

Overall, this project is still quite lacking. No Databases, or APIs were used, or Containers such as Docker and K8s. 
However, this was valuable learning experience. Althought this might not seem like a huge project, this was still very time consuming
as I needed to learn the fundamentals of everything and to be quite frank there weren't many good quality resources online of what to do
especially if you were on a budget. 


