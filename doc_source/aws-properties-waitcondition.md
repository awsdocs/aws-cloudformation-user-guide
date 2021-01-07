# AWS::CloudFormation::WaitCondition<a name="aws-properties-waitcondition"></a>

**Important**  
For Amazon EC2 and Auto Scaling resources, we recommend that you use a CreationPolicy attribute instead of wait conditions\. Add a CreationPolicy attribute to those resources, and use the cfn\-signal helper script to signal when an instance creation process has completed successfully\.

You can use a wait condition for situations like the following:
+ To coordinate stack resource creation with configuration actions that are external to the stack creation
+ To track the status of a configuration process

For these situations, we recommend that you associate a [CreationPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-creationpolicy.html) attribute with the wait condition so that you don't have to use a wait condition handle\. For more information and an example, see [Creating wait conditions in a template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-waitcondition.html)\. If you use a CreationPolicy with a wait condition, do not specify any of the wait condition's properties\.

**Note**  
If you use the [VPC endpoints](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html) feature, resources in the VPC that respond to wait conditions must have access to CloudFormation\-specific Amazon Simple Storage Service \(Amazon S3\) buckets\. Resources must send wait condition responses to a pre\-signed Amazon S3 URL\. If they can't send responses to Amazon S3, CloudFormation won't receive a response and the stack operation fails\. For more information, see [Setting up VPC endpoints for AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-vpce-bucketnames.html)\.

## Syntax<a name="aws-properties-waitcondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-waitcondition-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::WaitCondition",
  "Properties" : {
      "[Count](#cfn-waitcondition-count)" : Integer,
      "[Handle](#cfn-waitcondition-handle)" : String,
      "[Timeout](#cfn-waitcondition-timeout)" : String
    }
}
```

### YAML<a name="aws-properties-waitcondition-syntax.yaml"></a>

```
Type: AWS::CloudFormation::WaitCondition
Properties: 
  [Count](#cfn-waitcondition-count): Integer
  [Handle](#cfn-waitcondition-handle): String
  [Timeout](#cfn-waitcondition-timeout): String
```

## Properties<a name="aws-properties-waitcondition-properties"></a>

`Count`  <a name="cfn-waitcondition-count"></a>
The number of success signals that CloudFormation must receive before it continues the stack creation process\. When the wait condition receives the requisite number of success signals, CloudFormation resumes the creation of the stack\. If the wait condition does not receive the specified number of success signals before the Timeout period expires, CloudFormation assumes that the wait condition has failed and rolls the stack back\.  
Updates are not supported\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Handle`  <a name="cfn-waitcondition-handle"></a>
A reference to the wait condition handle used to signal this wait condition\. Use the `Ref` intrinsic function to specify an [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html) resource\.  
Anytime you add a WaitCondition resource during a stack update, you must associate the wait condition with a new WaitConditionHandle resource\. Do not reuse an old wait condition handle that has already been defined in the template\. If you reuse a wait condition handle, the wait condition might evaluate old signals from a previous create or update stack command\.  
Updates are not supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-waitcondition-timeout"></a>
The length of time \(in seconds\) to wait for the number of signals that the `Count` property specifies\. `Timeout` is a minimum\-bound property, meaning the timeout occurs no sooner than the time you specify, but can occur shortly thereafter\. The maximum time that can be specified for this property is 12 hours \(43200 seconds\)\.  
Updates are not supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-waitcondition-return-values"></a>

### Ref<a name="aws-properties-waitcondition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-waitcondition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-waitcondition-return-values-fn--getatt-fn--getatt"></a>

`Data`  <a name="Data-fn::getatt"></a>
A JSON object that contains the `UniqueId` and `Data` values from the wait condition signal\(s\) for the specified wait condition\. For more information about wait condition signals, see [Wait condition signal JSON format](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-waitcondition.html#using-cfn-waitcondition-signaljson)\.  
Example return value for a wait condition with 2 signals:  
 `{ "Signal1" : "Step 1 complete." , "Signal2" : "Step 2 complete." }` 

## Examples<a name="aws-properties-waitcondition--examples"></a>



### WaitCondition that waits for the desired number of instances in a web server group<a name="aws-properties-waitcondition--examples--WaitCondition_that_waits_for_the_desired_number_of_instances_in_a_web_server_group"></a>



#### JSON<a name="aws-properties-waitcondition--examples--WaitCondition_that_waits_for_the_desired_number_of_instances_in_a_web_server_group--json"></a>

```
"WebServerGroup" : {
  "Type" : "AWS::AutoScaling::AutoScalingGroup",
  "Properties" : {
    "AvailabilityZones" : { "Fn::GetAZs" : "" },
    "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
    "MinSize" : "1",
    "MaxSize" : "5",
    "DesiredCapacity" : { "Ref" : "WebServerCapacity" },
    "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ]
  }
},
        
"WaitHandle" : {
  "Type" : "AWS::CloudFormation::WaitConditionHandle"
},
        
"WaitCondition" : {
  "Type" : "AWS::CloudFormation::WaitCondition",
  "DependsOn" : "WebServerGroup",
  "Properties" : {
    "Handle"  : { "Ref" : "WaitHandle" },
    "Timeout" : "300",
    "Count"   : { "Ref" : "WebServerCapacity" }
  }
}
```

#### YAML<a name="aws-properties-waitcondition--examples--WaitCondition_that_waits_for_the_desired_number_of_instances_in_a_web_server_group--yaml"></a>

```
WebServerGroup: 
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties: 
    AvailabilityZones: 
      Fn::GetAZs: ""
    LaunchConfigurationName: 
      Ref: "LaunchConfig"
    MinSize: "1"
    MaxSize: "5"
    DesiredCapacity: 
      Ref: "WebServerCapacity"
    LoadBalancerNames: 
      - 
        Ref: "ElasticLoadBalancer"
WaitHandle: 
  Type: AWS::CloudFormation::WaitConditionHandle
WaitCondition: 
  Type: AWS::CloudFormation::WaitCondition
  DependsOn: "WebServerGroup"
  Properties: 
    Handle: 
      Ref: "WaitHandle"
    Timeout: "300"
    Count: 
      Ref: "WebServerCapacity"
```

## See also<a name="aws-properties-waitcondition--seealso"></a>
+  [Creating wait conditions in a template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-waitcondition.html) 
+  [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) 

