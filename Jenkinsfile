pipeline{
    agent any

    environment {
        prueba = "Prueba de las variables"
    }

    stages{

        stage("Prueba de aprobaciones"){
            input{
                message "Desea inicializar?"
                ok "Si"
            }
            steps{
                echo "Comenzando deploy"
            }
        }
        stage("Instalar Dependencias"){
            steps{
                sh "npm install"
            }
        }
        stage("Compilacion del App"){
            steps{
                sh "npm run build"
            }
        }
        stage("Mostrar archivos"){
            steps{
                sh "ls -la"
            }
        }
        stage("Prueba variable"){
            steps{
                echo "${prueba}"
            }
        }
    /*post{
        always{
            emailext body: "Correo de prueba Sebas", subject: "prueba", to: "sebassolise2000@gmail.com"
        }
    }*/

        /*
        stage("Despliegue de la aplicacion"){
            steps{
                sh "cp /var/lib/jenkins/workspace/AngularAppSebas_main* /var/www/html"
            }
        }*/
    }
    post{
        always{
            emailext body: "Correo de prueba Sebas", subject: "prueba", to: "sebassolise2000@gmail.com"
        }
    }
}