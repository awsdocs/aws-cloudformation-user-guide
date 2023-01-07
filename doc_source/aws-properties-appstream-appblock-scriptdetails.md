# AWS::AppStream::AppBlock ScriptDetails<a name="aws-properties-appstream-appblock-scriptdetails"></a>

The details of the script\.

## Syntax<a name="aws-properties-appstream-appblock-scriptdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-appblock-scriptdetails-syntax.json"></a>

```
{
  "[ExecutableParameters](#cfn-appstream-appblock-scriptdetails-executableparameters)" : String,
  "[ExecutablePath](#cfn-appstream-appblock-scriptdetails-executablepath)" : String,
  "[ScriptS3Location](#cfn-appstream-appblock-scriptdetails-scripts3location)" : S3Location,
  "[TimeoutInSeconds](#cfn-appstream-appblock-scriptdetails-timeoutinseconds)" : Integer
}
```

### YAML<a name="aws-properties-appstream-appblock-scriptdetails-syntax.yaml"></a>

```
  [ExecutableParameters](#cfn-appstream-appblock-scriptdetails-executableparameters): String
  [ExecutablePath](#cfn-appstream-appblock-scriptdetails-executablepath): String
  [ScriptS3Location](#cfn-appstream-appblock-scriptdetails-scripts3location): 
    S3Location
  [TimeoutInSeconds](#cfn-appstream-appblock-scriptdetails-timeoutinseconds): Integer
```

## Properties<a name="aws-properties-appstream-appblock-scriptdetails-properties"></a>

`ExecutableParameters`  <a name="cfn-appstream-appblock-scriptdetails-executableparameters"></a>
The parameters used in the run path for the script\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecutablePath`  <a name="cfn-appstream-appblock-scriptdetails-executablepath"></a>
The run path for the script\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScriptS3Location`  <a name="cfn-appstream-appblock-scriptdetails-scripts3location"></a>
The S3 object location of the script\.  
*Required*: Yes  
*Type*: [S3Location](aws-properties-appstream-appblock-s3location.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeoutInSeconds`  <a name="cfn-appstream-appblock-scriptdetails-timeoutinseconds"></a>
The run timeout, in seconds, for the script\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)