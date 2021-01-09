# AWS::Config::ConfigurationRecorder<a name="aws-resource-config-configurationrecorder"></a>

The AWS::Config::ConfigurationRecorder resource describes the AWS resource types for which AWS Config records configuration changes\. The configuration recorder stores the configurations of the supported resources in your account as configuration items\. 

**Note**  
To enable AWS Config, you must create a configuration recorder and a delivery channel\. AWS Config uses the delivery channel to deliver the configuration changes to your Amazon S3 bucket or Amazon SNS topic\. For more information, see [AWS::Config::DeliveryChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-deliverychannel.html)\.

AWS CloudFormation starts the recorder as soon as the delivery channel is available\. To stop the recorder, delete the configuration recorder from your stack\. For more information, see [Configuration Recorder](https://docs.aws.amazon.com/config/latest/developerguide/config-concepts.html#config-recorder) in the AWS Config Developer Guide\. 

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
A name for the configuration recorder\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the configuration recorder name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
After you create a configuration recorder, you cannot rename it\. If you don't want a name that AWS CloudFormation generates, specify a value for this property\. 
Updates are not supported\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordingGroup`  <a name="cfn-config-configurationrecorder-recordinggroup"></a>
Indicates whether to record configurations for all supported resources or for a list of resource types\. The resource types that you list must be supported by AWS Config\.   
*Required*: No  
*Type*: [RecordingGroup](aws-properties-config-configurationrecorder-recordinggroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-config-configurationrecorder-rolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that is used to make read or write requests to the delivery channel that you specify and to get configuration details for supported AWS resources\. For more information, see [Permissions for the IAM Role Assigned](https://docs.aws.amazon.com/config/latest/developerguide/iamrole-permissions.html) to AWS Config in the AWS Config Developer Guide\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-configurationrecorder-return-values"></a>

### Ref<a name="aws-resource-config-configurationrecorder-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the configuration recorder name, such as default\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

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