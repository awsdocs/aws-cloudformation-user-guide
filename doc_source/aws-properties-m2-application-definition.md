# AWS::M2::Application Definition<a name="aws-properties-m2-application-definition"></a>

The application definition for a particular application\. You can specify either inline JSON or an Amazon S3 bucket location\.

## Syntax<a name="aws-properties-m2-application-definition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-m2-application-definition-syntax.json"></a>

```
{
  "[Content](#cfn-m2-application-definition-content)" : String,
  "[S3Location](#cfn-m2-application-definition-s3location)" : String
}
```

### YAML<a name="aws-properties-m2-application-definition-syntax.yaml"></a>

```
  [Content](#cfn-m2-application-definition-content): String
  [S3Location](#cfn-m2-application-definition-s3location): String
```

## Properties<a name="aws-properties-m2-application-definition-properties"></a>

`Content`  <a name="cfn-m2-application-definition-content"></a>
The content of the application definition\. This is a JSON object that contains the resource configuration/definitions that identify an application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Location`  <a name="cfn-m2-application-definition-s3location"></a>
The S3 bucket that contains the application definition\.  
*Required*: No  
*Type*: String  
*Pattern*: `\S{1,2000}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)