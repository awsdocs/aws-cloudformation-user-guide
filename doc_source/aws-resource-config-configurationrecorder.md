# AWS::Config::ConfigurationRecorder<a name="aws-resource-config-configurationrecorder"></a>

The `AWS::Config::ConfigurationRecorder` resource type describes the AWS resource types that AWS Config records for configuration changes\.

The configuration recorder stores the configuration changes of the specified resources in your account as configuration items\.

**Note**  
To enable AWS Config, you must create a configuration recorder and a delivery channel\.  
AWS Config uses the delivery channel to deliver the configuration changes to your Amazon S3 bucket or Amazon SNS topic\. For more information, see [AWS::Config::DeliveryChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-deliverychannel.html)\.

AWS CloudFormation starts the recorder as soon as the delivery channel is available\.

To stop the recorder and delete it, delete the configuration recorder from your stack\. To stop the recorder without deleting it, call the [StopConfigurationRecorder](https://docs.aws.amazon.com/config/latest/APIReference/API_StopConfigurationRecorder.html) action of the AWS Config API directly\.

For more information, see [Configuration Recorder](https://docs.aws.amazon.com/config/latest/developerguide/config-concepts.html#config-recorder) in the AWS Config Developer Guide\.

## Syntax<a name="aws-resource-config-configurationrecorder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-configurationrecorder-syntax.json"></a>

```
{
  "Type" : "AWS::Config::ConfigurationRecorder",
  "Properties" : {
      "[Name](#cfn-config-configurationrecorder-name)" : String,
      "[RecordingGroup](#cfn-config-configurationrecorder-recordinggroup)" : RecordingGroup,
      "[RoleARN](#cfn-config-configurationrecorder-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-config-configurationrecorder-syntax.yaml"></a>

```
Type: AWS::Config::ConfigurationRecorder
Properties: 
  [Name](#cfn-config-configurationrecorder-name): String
  [RecordingGroup](#cfn-config-configurationrecorder-recordinggroup): 
    RecordingGroup
  [RoleARN](#cfn-config-configurationrecorder-rolearn): String
```

## Properties<a name="aws-resource-config-configurationrecorder-properties"></a>

`Name`  <a name="cfn-config-configurationrecorder-name"></a>
The name of the configuration recorder\. AWS Config automatically assigns the name of "default" when creating the configuration recorder\.  
You cannot change the name of the configuration recorder after it has been created\. To change the configuration recorder name, you must delete it and create a new configuration recorder with a new name\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordingGroup`  <a name="cfn-config-configurationrecorder-recordinggroup"></a>
Specifies which resource types AWS Config records for configuration changes\.  
** High Number of AWS Config Evaluations**  
You may notice increased activity in your account during your initial month recording with AWS Config when compared to subsequent months\. During the initial bootstrapping process, AWS Config runs evaluations on all the resources in your account that you have selected for AWS Config to record\.  
If you are running ephemeral workloads, you may see increased activity from AWS Config as it records configuration changes associated with creating and deleting these temporary resources\. An *ephemeral workload* is a temporary use of computing resources that are loaded and run when needed\. Examples include Amazon Elastic Compute Cloud \(Amazon EC2\) Spot Instances, Amazon EMR jobs, and AWS Auto Scaling\. If you want to avoid the increased activity from running ephemeral workloads, you can run these types of workloads in a separate account with AWS Config turned off to avoid increased configuration recording and rule evaluations\.
*Required*: No  
*Type*: [RecordingGroup](aws-properties-config-configurationrecorder-recordinggroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-config-configurationrecorder-rolearn"></a>
Amazon Resource Name \(ARN\) of the IAM role assumed by AWS Config and used by the configuration recorder\. For more information, see [Permissions for the IAM Role Assigned](https://docs.aws.amazon.com/config/latest/developerguide/iamrole-permissions.html) to AWS Config in the AWS Config Developer Guide\.  
**Pre\-existing AWS Config role**  
If you have used an AWS service that uses AWS Config, such as AWS Security Hub or AWS Control Tower, and an AWS Config role has already been created, make sure that the IAM role that you use when setting up AWS Config keeps the same minimum permissions as the already created AWS Config role\. You must do this so that the other AWS service continues to run as expected\.   
For example, if AWS Control Tower has an IAM role that allows AWS Config to read Amazon Simple Storage Service \(Amazon S3\) objects, make sure that the same permissions are granted within the IAM role you use when setting up AWS Config\. Otherwise, it may interfere with how AWS Control Tower operates\. For more information about IAM roles for AWS Config, see [https://docs.aws.amazon.com/config/latest/developerguide/security-iam.html](https://docs.aws.amazon.com/config/latest/developerguide/security-iam.html) in the *AWS Config Developer Guide*\. 
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-configurationrecorder-return-values"></a>

### Ref<a name="aws-resource-config-configurationrecorder-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the configuration recorder name, such as default\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-configurationrecorder--examples"></a>



### Configuration Recorder<a name="aws-resource-config-configurationrecorder--examples--Configuration_Recorder"></a>

The following example creates a configuration recorder for EC2 volumes\.

#### JSON<a name="aws-resource-config-configurationrecorder--examples--Configuration_Recorder--json"></a>

```
"ConfigRecorder": {
  "Type": "AWS::Config::ConfigurationRecorder",
  "Properties": {
    "Name": "default",
    "RecordingGroup": {
      "ResourceTypes": ["AWS::EC2::Volume"]
    },
    "RoleARN": {"Fn::GetAtt": ["ConfigRole", "Arn"]}
  }
}
```

#### YAML<a name="aws-resource-config-configurationrecorder--examples--Configuration_Recorder--yaml"></a>

```
ConfigRecorder: 
  Type: AWS::Config::ConfigurationRecorder
  Properties: 
    Name: default
    RecordingGroup: 
      ResourceTypes: 
        - "AWS::EC2::Volume"
    RoleARN: 
      Fn::GetAtt: 
        - ConfigRole
        - Arn
```