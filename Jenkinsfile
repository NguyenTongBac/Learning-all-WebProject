pipeline{
    agent{
        label "my-agent"
    }
    stages{
        stage("clone"){
            steps{
                echo "========executing A========"
                git 'https://github.com/NguyenTongBac/Learning-all-WebProject.git'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
        stage("go direction")
        {
            steps{
                echo "========executing B========"
                cd Learning-all-WebProject
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========B executed successfully========"
                }
                failure{
                    echo "========B execution failed========"
                }
            }
        }
        stage("go direction")
        {
            steps{
                echo "========executing C========"
                dotnet --version
                dotnet clean
                dotnet build
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========C executed successfully========"
                }
                failure{
                    echo "========C execution failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}