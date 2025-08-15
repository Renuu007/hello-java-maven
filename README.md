# Hello Java Maven 🚀

A simple Java HelloWorld project built with Maven and integrated with Jenkins for CI/CD demonstration.

## 📦 Project Structure
```
hello-java-maven/
├── src/
│   └── main/
│       └── java/
│           └── HelloWorld.java
├── pom.xml
└── Jenkins_Build_Report.md
```

## 📝 Prerequisites
- Java JDK 8 or 11 ☕
- Maven 🛠️
- Jenkins (locally or via Docker) 🐳
- Git (optional) 🐙

## 📥 Clone the Repository
```sh
git clone https://github.com/Renuu007/hello-java-maven.git
cd hello-java-maven
```

## ⚙️ Build Locally with Maven
```sh
mvn clean package
```
- The output JAR will be in `target/hello-1.0.jar`

## 🐳 Run Jenkins with Docker
```sh
docker run -p 8080:8080 jenkins/jenkins:lts
```
- Access Jenkins at: http://localhost:8080

## 🛠️ Jenkins Setup Steps
1. Go to **Manage Jenkins** → **Global Tool Configuration**
2. Under **Maven**, click **Add Maven**
   - Name: `Maven 3.8.6` (or similar)
   - Check **Install automatically**
3. Save
4. Create a new **Freestyle project**
5. In **Build** section, add step: **Invoke top-level Maven targets**
   - Goals: `clean package`
   - Select the Maven version you configured
6. Save and **Build Now**
7. Check **Console Output** for `BUILD SUCCESS`



## 📊 Jenkins Build Report
See `Jenkins_Build_Report.md` for build screenshots and descriptions.

## 🔗 GitHub Repository
[https://github.com/Renuu007/hello-java-maven](https://github.com/Renuu007/hello-java-maven)

---

Made with ❤️ for CI/CD learning!
