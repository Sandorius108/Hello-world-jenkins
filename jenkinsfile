    pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compilando el código fuente...'
                // Para un proyecto real, aquí irían comandos como:
                // sh 'mvn clean install' o 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                // Aquí irían comandos para ejecutar pruebas, como:
                // sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación a un entorno de prueba...'
                // En un escenario real, esto podría construir una imagen Docker
                // y desplegarla en un servidor.
                archiveArtifacts artifacts: 'index.html', followSymlinks: false
            }
        }
    }
    post {
        success {
            echo 'Pipeline ejecutado exitosamente!'
        }
        failure {
            echo 'El pipeline ha fallado.'
        }
    }
}
