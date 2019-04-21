def context
def stageName
context = getBuildContext()

timestamps{
   prepareEnv(context, 'prepare')
   mediaInit(context, 'Initialization')
   mediaCodeDeployment(context, 'Deployment')
   mediaFinish(context, 'Finish')
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



def hello(context){
  if (context.environment == 'QA'){
    echo 'QA env'
  }
}

def prepareEnv(context, stageName){
  stage(stageName){
     if (context.environment == 'QA'){
       echo 'QA env'
     } else {
       echo context.environment 
     }
  }
}

def mediaInit(context, stageName){
   stage(stageName){
      println(stageName)
   }
}

def mediaCodeDeployment(context, stageName){
   stage(stageName){
      println(stageName)
   }
}

def mediaFinish(context, stageName){
   stage(stageName){
      println(stageName)
   }
}
