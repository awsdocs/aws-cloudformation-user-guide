# Amazon EC2 Auto Scaling AutoScalingGroup TagProperty<a name="aws-properties-as-tags"></a>

The `TagProperty` property type adds tags to all associated instances in an Amazon EC2 Auto Scaling group\.

The `Tags` property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource contains a list of `TagProperty` property types\. For more information, see [Tagging Auto Scaling Groups and Instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-tagging.html) in the *Amazon EC2 Auto Scaling User Guide*\.

AWS CloudFormation adds the following tags to all Auto Scaling groups and associated instances:
+ aws:cloudformation:stack\-name
+ aws:cloudformation:stack\-id
+ aws:cloudformation:logical\-id

## Syntax<a name="w4ab1c21c10c36c13c55c11"></a>

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

## Properties<a name="w4ab1c21c10c36c13c55c13"></a>

`Key`  <a name="cfn-as-tags-Key"></a>
The key name of the tag\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-as-tags-Value"></a>
The value for the tag\.  
*Required*: Yes  
*Type*: String

`PropagateAtLaunch`  <a name="cfn-as-tags-PropagateAtLaunch"></a>
Set to `true` if you want AWS CloudFormation to copy the tag to EC2 instances that are launched as part of the Auto Scaling group\. Set to `false` if you want the tag attached only to the Auto Scaling group and not copied to any instances launched as part of the Auto Scaling group\.  
*Required*: Yes  
*Type*: Boolean

## Example<a name="aws-properties-as-tags-examples"></a>

The following example template snippet creates two tags\. The first tag, `MyTag1`, is attached to an Auto Scaling group named `WebServerGroup` and is copied to any EC2 instances launched as part of the Auto Scaling group\. The second tag, `MyTag2`, is attached only to the Auto Scaling group named `WebServerGroup`\.

### JSON<a name="aws-properties-as-tags-example.json"></a>

```
 1. "WebServerGroup" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "AvailabilityZones" : { 
 5.          "Fn::GetAZs" : "" 
 6.       },
 7.       "LaunchConfigurationName" : { 
 8.          "Ref" : "LaunchConfig" 
 9.       },
10.       "MinSize" : "1",
11.       "MaxSize" : "2",
12.       "LoadBalancerNames" : [ 
13.          { 
14.             "Ref" : "ElasticLoadBalancer" 
15.          } 
16.       ],
17.       "Tags" : [ 
18.          {
19.             "Key" : "MyTag1",
20.             "Value" : "Hello World 1",
21.             "PropagateAtLaunch" : "true"
22.          }, 
23.          {
24.             "Key" : "MyTag2",
25.             "Value" : "Hello World 2",
26.             "PropagateAtLaunch" : "false"
27.          } 
28.       ]
29.    }
30. }
```

### YAML<a name="aws-properties-as-tags-example.yaml"></a>

```
 1. WebServerGroup:
 2.   Type: 'AWS::AutoScaling::AutoScalingGroup'
 3.   Properties:
 4.     AvailabilityZones: !GetAZs ''
 5.     LaunchConfigurationName: !Ref LaunchConfig
 6.     MinSize: '1'
 7.     MaxSize: '2'
 8.     LoadBalancerNames:
 9.       - !Ref ElasticLoadBalancer
10.     Tags:
11.       - Key: MyTag1
12.         Value: Hello World 1
13.         PropagateAtLaunch: 'true'
14.       - Key: MyTag2
15.         Value: Hello World 2
16.         PropagateAtLaunch: 'false'
```