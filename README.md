 # 2 pipeline
 New Item → Freestyle Project

Keep:

SCM

Git URL: https://github.com/bhavagna06/Maven.git

Branch: */main (or) */master

# Build Steps

1️⃣ Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: clean

2️⃣ Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: install

# Post-Build Actions

Archive artifacts: **/*

Build other projects: MavenJava_Test

Trigger: Only if build is stable

Save.

✅ Step 3 — Create Test Job (MavenJava_Test)
# Build Environment

✔ Delete workspace before build

# Copy Artifacts

Project name: MavenJava_Build

Build: Stable only

Artifacts: **/*

Build Step

Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: test

Post-Build Actions

Archive artifacts: **/*

Save.



# 3 pipeline


🌐 Maven Web Automation — Short & Clear Steps
✅ Step 1 — Build Job (MavenWeb_Build)

New Item → Freestyle Project

Name: MavenWeb_Build

SCM

Git URL: https://github.com/bhavagna06/maven-web-app.git

Branch: */main or */master

Build Steps

1️⃣ Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: clean

2️⃣ Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: install

Post-Build Actions

Archive artifacts: **/*

Build other projects: MavenWeb_Test

Trigger: Only if build is stable

Save.

✅ Step 2 — Test Job (MavenWeb_Test)
Build Environment

✔ Delete workspace before build starts

Copy Artifacts

Project name: MavenWeb_Build

Build: Stable only

Artifacts: **/*

Build Step

Invoke top-level Maven targets

Maven version: MAVEN_HOME

Goals: test

Post-Build Actions

Archive artifacts: **/*

Build other projects: MavenWeb_Deploy

Save.

✅ Step 3 — Deploy Job (MavenWeb_Deploy)
Build Environment

✔ Delete workspace before build starts

Copy Artifacts

Project name: MavenWeb_Test

Build: Stable only

Artifacts: **/*

Post-Build Actions

Deploy WAR/EAR to a container

WAR/EAR File: **/*.war

Context path: Webpath

Container: Tomcat 9.x remote

Credentials: admin / 1234

Tomcat URL: http://localhost:8080/

Save.

🎯 Pipeline View

Create → MavenWeb_Pipeline

Initial Job: MavenWeb_Build



# nagios

1.docker pull jasonrivers/nagios:latest
2.docker run --name nagiosdemo1 --p 8888:80 jasonrivers/nagios:latest
