pipeline {
  agent any
  def context = getBuildContext{}
  timestamps{
    stage('first'){
      prepareEnv(context)
    }
    stage('second'){
      hello(context)
    }
  }
}

def prepareEnv(context){
   println(context.environment)
}

def hello(context){
  println('Hello')
}
