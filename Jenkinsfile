pipeline{
    agent any

    stages{
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
                sh "ls -l"
            }
        }
        stage("Despliegue de la aplicacion"){
            steps{
                sh "cp dist/AngularAppSebas_main* var/www/html"
            }
        }
    }
}
