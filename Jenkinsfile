pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'STAGE 1: BUILD'
                echo 'This stage compiles and packages the application using a build tool such as Maven or Gradle.'
                echo 'In a real project, this would produce a deployable artifact (e.g., JAR or WAR file).'
                // Example (not executed here):
                // sh 'mvn clean package'
            }
        }

        stage('Unit & Integration Tests') {
            steps {
                echo 'STAGE 2: UNIT & INTEGRATION TESTS'
                echo 'This stage runs automated unit and integration tests to validate application functionality.'
                echo 'Common tools include JUnit for unit testing and Selenium for integration testing.'
                // Example:
                // sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'STAGE 3: CODE ANALYSIS'
                echo 'This stage performs static code analysis to check code quality, bugs, and coding standards.'
                echo 'SonarQube is commonly used to identify code smells and technical debt.'
                // Example:
                // sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'STAGE 4: SECURITY SCAN'
                echo 'This stage scans project dependencies for known security vulnerabilities.'
                echo 'OWASP Dependency-Check is used to identify vulnerable third-party libraries.'
                // Example:
                // sh 'dependency-check.sh'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'STAGE 5: DEPLOY TO STAGING'
                echo 'This stage deploys the application to a staging environment hosted on AWS EC2.'
                echo 'Staging closely mirrors the production environment for final validation.'
                // Example:
                // sh 'scp target/app.jar ec2-user@staging-server:/app'
            }
        }

        stage('Integration Tests (Staging)') {
            steps {
                echo 'STAGE 6: INTEGRATION TESTS (STAGING)'
                echo 'This stage executes integration and end-to-end tests in the staging environment.'
                echo 'Tools such as Postman or Selenium are used to verify system behaviour.'
                // Example:
                // sh 'newman run api-tests.json'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'STAGE 7: DEPLOY TO PRODUCTION'
                echo 'This stage deploys the stable and tested build to the production environment on AWS EC2.'
                echo 'Only validated releases are deployed to ensure system stability.'
                // Example:
                // sh 'scp target/app.jar ec2-user@production-server:/app'
            }
        }
    }
}
