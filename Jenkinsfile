  
pipeline {
         agent any
         stages {
                 stage('Unit Testing') {
                 steps {
                     echo 'Unit Test Passed'
                 }
                 }
                 stage('Integration Testing') {
                 steps {

                  echo 'Running Integrations'
                  echo 'Passed Integrations Testing'
                 }

                 }

                 stage('Browser Testing') {
                 parallel { 
                            stage('Chrome testing') {
                          
                                steps {
                    input('Did Chrome testing pass ?')
                 }
                           
                           }
                            stage('Internet Explorer Testing') {
                              
                              steps {
                    input('Did IE testing pass ?')
                                
                              }
                           }
                           }
                           }


                 stage('Acceptance Testing') {
                 steps {
                    echo 'Unit Test Passed'                 }
                 }
                 }
                 stage('Exploratory Testing') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }

                 stage('Staging') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Preproduction Deployment') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Production Deployment') {
                 steps {
                    echo 'deployed on Production'
                 }
                 }
                 
             } 
