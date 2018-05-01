pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/narendrasingamaneni91/Robopython.git', branch: 'master', credentialsId: 'narendrasingamaneni91')
      }
    }
    stage('build') {
      steps {
        echo 'build'
        sh '''#!/bin/bash
source /opt/ros/kinetic/setup.bash
source titan/catkin_ws/devel/setup.bash
rosrun decisionmanagement decisionmanagement_node &
export GOOGLE_APPLICATION_CREDENTIALS=/home/vishnun/googleapis/gens
export GOOGLE_APPLICATION_CREDENTIALS=/home/vishnun/voice_credentials.json
g++ -o sonus/robovoice/ruta_speechrecognition sonus/robovoice/ruta_speechrecognition.cpp
cd apollo
chmod +x demo_annotate_train.sh
./demo_annotate_train.sh
chmod +x demo_annotateVideo_train.sh
./demo_annotateVideo_train.sh
chmod +x test_demo_annotate_train.sh
./test_demo_annotate_train.sh
chmod +x test_update_ownership_demo_annotate_train.sh
./test_update_ownership_demo_annotate_train.sh
chmod +x test_demo_annotateVideo_train.sh
./test_demo_annotateVideo_train.sh
chmod +x test_update_ownership_demo_annotateVideo_train.sh
./test_update_ownership_demo_annotateVideo_train.sh'''
      }
    }
  }
}