def context
def script
context = getBuildContext()

timestamps{
  stage('first'){
    hello(context, script)
  }
  stage('second'){
    echo 'hello...'
  }
}

def getBuildContext(){
  def context = [:]
  context.environment = env.ENVIRONMENT ? env.ENVIRONMENT.toUpperCase() : params.ENVIRONMENT?.toUpperCase()
	context.ENVIRONMENT_ID = env.ENVIRONMENT_ID ? env.ENVIRONMENT_ID.toLowerCase() : params.ENVIRONMENT_ID?.toLowerCase()
	context.ENVIRONMENT = env.ENVIRONMENT ? env.ENVIRONMENT.toUpperCase() : params.ENVIRONMENT?.toUpperCase()
	context.BUILD_PIPELINE = env.BUILD_PIPELINE ? env.BUILD_PIPELINE : params.BUILD_PIPELINE
	context.param_branch = env.BRANCH ? env.BRANCH : params.BRANCH
	context.param_tag = env.TAG ? env.TAG : params.TAG
	context.build_number = env.BUILD_NUMBER
  return context
}

def hello(context, script){
  this.script = script
  if (context.environment == 'QA'){
    script.sh 'QA env'
  }
}
