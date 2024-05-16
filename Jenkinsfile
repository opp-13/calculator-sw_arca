pipeline { 
     agent any 
     stages { 
          stage("Compile") { 
               steps { 
                    sh "./gradlew compileJava"
                    sh "chmod 777 ./gradlew"
               } 
          }
            stage("Build") {
                         steps {
                              sh "chmod +x ./gradlew"
                              sh "./gradlew build"
                         }
                    }

          stage("Unit test") { 
               steps { 
                    sh "./gradlew test" 
               } 
          } 
     } 
}
