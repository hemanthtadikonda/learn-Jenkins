def X = 10
def Z = 20
env.Y = 30
def sample(){
   print "XYZ function"
}




node ('slave') {
   stage ('test'){
   print X
   }
   stage('code'){
   print Z
   }
   stage('compile'){
   sh 'echo y -${Y}'
   sample()
   }
}