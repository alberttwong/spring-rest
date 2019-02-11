apiVersion: build.openshift.io/v1
kind: BuildConfig
metadata:
  name: spring-rest-build
spec:
  runPolicy: Serial
  source:
    git:
      ref: master
      uri: "https://github.com/alberttwong/spring-rest"
    type: Git
  strategy:
    jenkinsPipelineStrategy:
      env:
      jenkinsfilePath: Jenkinsfile.standalone
    type: JenkinsPipeline
  triggers:
    - github:
        secret: CqPGlXcKJXXqKxW4Ye6z
      type: GitHub
    - generic:
        secret: 4LXwMdx9vhQY4WXbLcFR
      type: Generic
    - type: ConfigChange
