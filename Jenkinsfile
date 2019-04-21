timestamps{
  stage('first'){
    hello('first')
    getBuildContext()
  }
  stage('second'){
    hello('second')
  }
}
def context
def script
def getBuildContext(){
  context = getContext()
  println(context)
}



def hello(str){
  println(str)
}
