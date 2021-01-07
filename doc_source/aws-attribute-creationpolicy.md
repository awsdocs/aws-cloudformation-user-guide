# CreationPolicy attribute<a name="aws-attribute-creationpolicy"></a>

Associate the `CreationPolicy` attribute with a resource to prevent its status from reaching create complete until AWS CloudFormation receives a specified number of success signals or the timeout period is exceeded\. To signal a resource, you can use the [cfn\-signal](cfn-signal.md) helper script or [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SignalResource.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SignalResource.html) API\. AWS CloudFormation publishes valid signals to the stack events so that you track the number of signals sent\.

The creation policy is invoked only when AWS CloudFormation creates the associated resource\. Currently, the only AWS CloudFormation resources that support creation policies are [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html), [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html), and [AWS::CloudFormation::WaitCondition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitcondition.html)\.

Use the `CreationPolicy` attribute when you want to wait on resource configuration actions before stack creation proceeds\. For example, if you install and configure software applications on an EC2 instance, you might want those applications to be running before proceeding\. In such cases, you can add a `CreationPolicy` attribute to the instance, and then send a success signal to the instance after the applications are installed and configured\. For a detailed example, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

## Syntax<a name="w7739ab1c33c23b7b9"></a>

### JSON<a name="aws-attribute-creationpolicy-syntax.json"></a>

```
"CreationPolicy" : {
  "AutoScalingCreationPolicy" : {
    "MinSuccessfulInstancesPercent" : Integer
  },
  "ResourceSignal" : {    
    "Count" : Integer,
    "Timeout" : String
  }
}
```

### YAML<a name="aws-attribute-creationpolicy-syntax.yaml"></a>

```
CreationPolicy:
  AutoScalingCreationPolicy:
    MinSuccessfulInstancesPercent: Integer
  ResourceSignal:    
    Count: Integer
    Timeout: String
```

## CreationPolicy properties<a name="cfn-attributes-creationpolicy-properties"></a>

`AutoScalingCreationPolicy`  <a name="cfn-attributes-creationpolicy-autoscalingcreationpolicy"></a>
For an Auto Scaling group [replacement update](aws-attribute-updatepolicy.md#cfn-attributes-updatepolicy-replacingupdate), specifies how many instances must signal success for the update to succeed\.    
`MinSuccessfulInstancesPercent`  <a name="cfn-attributes-creationpolicy-autoscalingcreationpolicy-minsuccessfulinstancespercent"></a>
Specifies the percentage of instances in an Auto Scaling replacement update that must signal success for the update to succeed\. You can specify a value from `0` to `100`\. AWS CloudFormation rounds to the nearest tenth of a percent\. For example, if you update five instances with a minimum successful percentage of `50`, three instances must signal success\. If an instance doesn't send a signal within the time specified by the `Timeout` property, AWS CloudFormation assumes that the instance wasn't created\.  
*Default*: `100`  
*Type*: Integer  
*Required*: No

`ResourceSignal`  <a name="cfn-attributes-creationpolicy-resourcesignal"></a>
When AWS CloudFormation creates the associated resource, configures the number of required success signals and the length of time that AWS CloudFormation waits for those signals\.    
`Count`  <a name="cfn-attributes-creationpolicy-resourcesignal-count"></a>
The number of success signals AWS CloudFormation must receive before it sets the resource status as `CREATE_COMPLETE`\. If the resource receives a failure signal or doesn't receive the specified number of signals before the timeout period expires, the resource creation fails and AWS CloudFormation rolls the stack back\.  
*Default*: `1`  
*Type*: Integer  
*Required*: No  
`Timeout`  <a name="cfn-attributes-creationpolicy-resourcesignal-timeout"></a>
The length of time that AWS CloudFormation waits for the number of signals that was specified in the `Count` property\. The timeout period starts after AWS CloudFormation starts creating the resource, and the timeout expires no sooner than the time you specify but can occur shortly thereafter\. The maximum time that you can specify is 12 hours\.  
The value must be in [ISO8601 duration format](http://en.wikipedia.org/wiki/ISO_8601#Durations), in the form: "PT*\#*H*\#*M*\#*S", where each *\#* is the number of hours, minutes, and seconds, respectively\. For best results, specify a period of time that gives your instances plenty of time to get up and running\. A shorter timeout can cause a rollback\.  
*Default*: `PT5M` \(5 minutes\)  
*Type*: String  
*Required*: No

## Examples<a name="w7739ab1c33c23b7c13"></a>

### Auto Scaling group<a name="w7739ab1c33c23b7c13b2"></a>

The following example shows how to add a creation policy to an Auto Scaling group\. The creation policy requires three success signals and times out after 15 minutes\.

To have instances wait for an Elastic Load Balancing health check before they signal success, add a health\-check verification by using the [cfn\-init](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-init.html) helper script\. For an example, see the `verify_instance_health` command in the [Auto Scaling rolling updates](https://github.com/awslabs/aws-cloudformation-templates/blob/master/aws/services/AutoScaling/AutoScalingRollingUpdates.yaml) sample template\.

#### JSON<a name="aws-attribute-creationpolicy-example-1.json"></a>

```
"AutoScalingGroup": {
  "Type": "AWS::AutoScaling::AutoScalingGroup",
  "Properties": {
    "AvailabilityZones": { "Fn::GetAZs": "" },
    "LaunchConfigurationName": { "Ref": "LaunchConfig" },
    "DesiredCapacity": "3",
    "MinSize": "1",
    "MaxSize": "4"
  },
  "CreationPolicy": {
    "ResourceSignal": {
      "Count": "3",
      "Timeout": "PT15M"
    }
  },
  "UpdatePolicy" : {
    "AutoScalingScheduledAction" : {
      "IgnoreUnmodifiedGroupSizeProperties" : "true"
    },
    "AutoScalingRollingUpdate" : {
      "MinInstancesInService" : "1",
      "MaxBatchSize" : "2",
      "PauseTime" : "PT1M",
      "WaitOnResourceSignals" : "true"
    }
  }
},
"LaunchConfig": {
  "Type": "AWS::AutoScaling::LaunchConfiguration",
  "Properties": {
    "ImageId": "ami-16d18a7e",
    "InstanceType": "t2.micro",
    "UserData": {
      "Fn::Base64": {
        "Fn::Join" : [ "", [
          "#!/bin/bash -xe\n",
          "yum install -y aws-cfn-bootstrap\n",
          "/opt/aws/bin/cfn-signal -e 0 --stack ", { "Ref": "AWS::StackName" },
          " --resource AutoScalingGroup ",
          " --region ", { "Ref" : "AWS::Region" }, "\n"
        ] ]
      }
    }
  }
}
```

#### YAML<a name="aws-attribute-creationpolicy-example-1.yaml"></a>

```
AutoScalingGroup:
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties:
    AvailabilityZones:
      Fn::GetAZs: ''
    LaunchConfigurationName:
      Ref: LaunchConfig
    DesiredCapacity: '3'
    MinSize: '1'
    MaxSize: '4'
  CreationPolicy:
    ResourceSignal:
      Count: '3'
      Timeout: PT15M
  UpdatePolicy:
    AutoScalingScheduledAction:
      IgnoreUnmodifiedGroupSizeProperties: 'true'
    AutoScalingRollingUpdate:
      MinInstancesInService: '1'
      MaxBatchSize: '2'
      PauseTime: PT1M
      WaitOnResourceSignals: 'true'
LaunchConfig:
  Type: AWS::AutoScaling::LaunchConfiguration
  Properties:
    ImageId: ami-16d18a7e
    InstanceType: t2.micro
    UserData:
      "Fn::Base64":
        !Sub |
          #!/bin/bash -xe
          yum update -y aws-cfn-bootstrap
          /opt/aws/bin/cfn-signal -e $? --stack ${AWS::StackName} --resource AutoScalingGroup --region ${AWS::Region}
```

### WaitCondition<a name="w7739ab1c33c23b7c13b4"></a>

The following example shows how to add a creation policy to a wait condition\.

#### JSON<a name="aws-attribute-creationpolicy-example-2.json"></a>

```
"WaitCondition" : {
    "Type" : "AWS::CloudFormation::WaitCondition",
    "CreationPolicy" : {
        "ResourceSignal" : {
            "Timeout" : "PT15M",
            "Count" : "5"
        }
    }
}
```

#### YAML<a name="aws-attribute-creationpolicy-example-2.yaml"></a>

```
WaitCondition:
  Type: AWS::CloudFormation::WaitCondition
  CreationPolicy:
    ResourceSignal:
      Timeout: PT15M
      Count: 5
```