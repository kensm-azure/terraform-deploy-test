pipeline {
    agent any
    tools {
        "org.jenkinsci.plugins.terraform.TerraformInstallation" "terraform"
    }

    stages {
        stage('Terraform Init'){
            steps {
                    sh 'terraform --version'
                }
            }
        }
    }
}
