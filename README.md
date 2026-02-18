project: Jenkins CI Pipeline using AWS EC2, GitHub and Email Notifications

steps_completed:
  - Launched an AWS EC2 instance and installed Java, Git and Jenkins.
  - Configured Jenkins and installed required plugins (Git, GitHub, Email Extension).
  - Created a GitHub repository containing a Python script and Jenkinsfile.
  - Created a Jenkins Pipeline job that pulls code from GitHub and runs the build.
  - Configured Gmail SMTP in Jenkins to send build notifications via email.
  - Integrated GitHub Webhook to automatically trigger Jenkins build on every git push.

result:
  - Any push to GitHub automatically triggers Jenkins pipeline.
  - Jenkins runs the build and sends email notification with build status.
