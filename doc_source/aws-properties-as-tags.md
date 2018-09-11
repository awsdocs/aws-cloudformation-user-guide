# Amazon EC2 Auto Scaling AutoScalingGroup TagProperty<a name="aws-properties-as-tags"></a>

The `TagProperty` property type adds tags to all associated instances in an Auto Scaling group\.

The `Tags` property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource contains a list of `TagProperty` property types\. For more information about Auto Scaling tags, see [Tagging Auto Scaling Groups and Instances](http://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\.

AWS CloudFormation adds the following tags to all Auto Scaling groups and associated instances:
+ aws:cloudformation:stack\-name
+ aws:cloudformation:stack\-id
+ aws:cloudformation:logical\-id

## Syntax<a name="w3ab2c21c14d112c11"></a>

### JSON<a name="aws-properties-as-tags-syntax.json"></a>

```
{
   "[Key](#cfn-as-tags-Key)" : String,
   "[Value](#cfn-as-tags-Value)" : String,
   "[PropagateAtLaunch](#cfn-as-tags-PropagateAtLaunch)" : Boolean
}
```

### YAML<a name="aws-properties-as-tags-syntax.yaml"></a>

```
[Key](#cfn-as-tags-Key): String
[Value](#cfn-as-tags-Value): String
[PropagateAtLaunch](#cfn-as-tags-PropagateAtLaunch): Boolean
```

## Properties<a name="w3ab2c21c14d112c13"></a>

`Key`  <a name="cfn-as-tags-Key"></a>
The key name of the tag\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-as-tags-Value"></a>
The value for the tag\.  
*Required*: Yes  
*Type*: String

`PropagateAtLaunch`  <a name="cfn-as-tags-PropagateAtLaunch"></a>
Set to `true` if you want AWS CloudFormation to copy the tag to EC2 instances that are launched as part of the auto scaling group\. Set to `false` if you want the tag attached only to the auto scaling group and not copied to any instances launched as part of the auto scaling group\.  
*Required*: Yes  
*Type*: Boolean

## Example<a name="aws-properties-as-tags-examples"></a>

The following example template snippet creates two Auto Scaling tags\. The first tag, `MyTag1`, is attached to an Auto Scaling group named `WebServerGroup` and is copied to any EC2 instances launched as part of the Auto Scaling group\. The second tag, `MyTag2`, is attached only to the Auto Scaling group named `WebServerGroup`\.

### JSON<a name="aws-properties-as-tags-example.json"></a>

```
"WebServerGroup" : {
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Fn::GetAZs" : "" },
      "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
      "MinSize" : "1",
      "MaxSize" : "2",
      "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ],
      "Tags" : [ {
         "Key" : "MyTag1",
         "Value" : "Hello World 1",
         "PropagateAtLaunch" : "true"
      }, {
         "Key" : "MyTag2",
         "Value" : "Hello World 2",
         "PropagateAtLaunch" : "false"
      } ]
   }
}
```

### YAML<a name="aws-properties-as-tags-example.yaml"></a>

```
WebServerGroup:
  Type: 'AWS::AutoScaling::AutoScalingGroup'
  Properties:
    AvailabilityZones: !GetAZs ''
    LaunchConfigurationName: !Ref LaunchConfig
    MinSize: '1'
    MaxSize: '2'
    LoadBalancerNames:
      - !Ref ElasticLoadBalancer
    Tags:
      - Key: MyTag1
        Value: Hello World 1
        PropagateAtLaunch: 'true'
      - Key: MyTag2
        Value: Hello World 2
        PropagateAtLaunch: 'false'
```