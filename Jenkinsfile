def X = 10
def Z = 20
env.Y = 30
def sample(){
   print "XYZ function"
}




node ('slave') {
   if ( X > 10 ) {
      stage ('test'){
      print X
      }
   }else {
       stage('code'){
       print Z
       sample()
       }
   }
   stage('compile'){
   sh 'echo y -${Y}'
   sample()
   }
}