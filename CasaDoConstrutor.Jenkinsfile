pipeline {
    agent{ 
        label 'MASTER'
    }
    parameters {
            string(name: 'teste', defaultValue: "Revenda360QAS", description: 'Parametro teste.')
            booleanParam(name: 'Verbose', defaultValue: false, description: 'Verbose')
    }
    environment {
        XPTO = "Environment Teste"
    }        
    stages {
        stage("Checkout package.xml"){
            steps{
                script {
                    echo "teste :D"                        
                    echo "XPTO: $XPTO"
                }
            }
        }
    }
    post{
        // always{
        //     deleteDir()
        // }
        success{
            echo "Pipeline executado com sucesso!"
        }
        failure{
            echo "Pipeline executado com falhas"  
        }
    }
} 