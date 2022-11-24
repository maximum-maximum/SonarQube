# SonarQube

## Demo

Launching the SonarQube environment:

```zsh
$ git clone https://github.com/maximum-maximum/SonarQube.git
$ cd SonarQube
$ docker-compose up -d
```

Setup and analysis of SonarScanner:

```zsh
$ cd <TARGET_DIRECTORY>
$ PROJECT_NAME=<PROJECT_NAME> PROJECT_TOKEN=<PROJECT_TOKEN>
$ docker run \
--rm \
--net host \
-e SONAR_HOST_URL="http://localhost:9000" \
-v ${PWD}:/usr/src \
sonarsource/sonar-scanner-cli \
-Dsonar.projectKey=${PROJECT_NAME} \
-Dsonar.sonar.projectName=${PROJECT_NAME} \
-Dsonar.sonar.projectVersion=1.0 \
-Dsonar.sonar.sourceEncoding=UTF-8 \
-Dsonar.sonar.host.url=http://localhost:9000 \
-Dsonar.login=${PROJECT_TOKEN}
```

## Link

- Official: <https://www.sonarqube.org/>
- Official Github: <https://github.com/SonarSource/sonarqube>
