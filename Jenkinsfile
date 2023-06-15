pipeline{
    agent any

  enviroment{
    prueba = "Pruebas de variables"
  }  
    stages{
      stage("Prueba de variables"){
        steps{
          echo "${prueba}"
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
                sh "ls -l"
            }
        }
        stage("Despliegue de la aplicacion"){
            steps{
                sh "cp dist/AngularAppSebas* var/www/html"
            }
        }
    }
}
