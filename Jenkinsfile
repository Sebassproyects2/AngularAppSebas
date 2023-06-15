pipeline{
    agent any

    enviroment {
        prueba = "Prueba de las variables"
    }

    stages{

        stage("Prueba variable"){
            steps{
                echo "{prueba}"
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
        /*
        stage("Despliegue de la aplicacion"){
            steps{
                sh "cp /var/lib/jenkins/workspace/AngularAppSebas_main* /var/www/html"
            }
        }*/
    }
}