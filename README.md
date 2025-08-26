# Jenkins_Zero_Hero

<p>Welcome! This repository is your one-stop guide to mastering Jenkins — from the very basics to advanced CI/CD pipelines. Whether you're new to Jenkins or looking to sharpen your skills, this course will take you step-by-step through everything you need to know to become a Jenkins pro. </p>

**What is Jenkins** </br>
<p>Jenkins is an open-source automation server widely used to implement Continuous Integration (CI) and Continuous Delivery (CD) pipelines. It helps developers automate the process of building, testing, and deploying applications, making software development faster, more reliable, and more efficient.</p>

**Why Jenkins** </br>
<p>
  <ul>
    <li>Open Source: Jenkins is Open Source and Supported by Large Actice Community</li>
    <li>Extensible: With over 1800+ plugins, Jenkins integrates with almost any tool in your DevOps toolchain</li>
    <li>Easy To Use: Provide GUI and also Pipeline as Code using Jenkins file </li>
    <li>Highly Customizable</li>
  </ul>
</p>

**Installation of Jenkins** </br>

<p>There are Several different ways to Install Jenkins</p>
<ul>
  <li>Native Package Installation: Directly installing it on Linux Machine using package installer like apt, yum</li>
  <li>Docker Container: Use Docker to quickly run isolated, portable Jenkins instances ideal for testing, development, and containerized CI/CD workflows </li>
  <li>War File: Use the WAR file to quickly run Jenkins without installation—perfect for lightweight, temporary setups or testing</li>
  <li>Cloud Based Jenkins: Some cloud providers offer Jenkins pre-configured or managed as part of their DevOps offerings (e.g., AWS CodeBuild with Jenkins integration).</li>
</ul>

**Installing Jenkins on Google Compute Engine**

Youtube Video ->

**Creating Virtual Machine in GCP**


**Run the below commands to Install Jenkins**

Install Java

```
sudo apt update
sudo apt install openjdk-17-jre
```

Verify Java is Installed

```
java -version
```

Now, you can proceed with installing Jenkins

```
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

**Note: ** By default, Jenkins will not be accessible to the external world due to the inbound traffic restriction by AWS. Open port 8080 in the inbound traffic rules as show below.


