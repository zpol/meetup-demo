This is a .drone-yml example file: 

Here you can find some example about how to confihure a pipeline with drone-server: 


### In this example we deploy some code from our repo by using SCP plugin
and slack plugin to notify to a slack channel the build result: 


```
pipeline:

  scp:
    image: appleboy/drone-scp
    host: 1.2.3.4
    username: deployer
    password: ********
    port: 22
    target: /var/www/html/
    source: index.html



  slack:
    image: plugins/slack
    webhook: https://hooks.slack.com/services/XXXXXXXX/YYYYYYYY/zzzzzzzzzzzzzzzzzz
    channel: #demos
    icon_emoji: http://blah.com/images/logo_mini_compiler.jpg
    when:
      status: [ success, failure ]
   ```   
      
      
      
      
      
### Also we can validate and deploy entire stacks by using Cloud Formation:       
      

```
pipeline:
  validate-template:
    image: robertstettner/drone-cloudformation
    mode: validate
    template: templates/stack.yml
``` 
    
