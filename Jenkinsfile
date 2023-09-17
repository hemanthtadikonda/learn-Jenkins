node ('slave') {
   def X = 10
   def Z = 20
   env.Y = 30
   stage ('test'){
   print X
   }
   stage('code'){
   print Z
   }
   stage('compile'){
   sh 'echo y -${Y}'
   }
}