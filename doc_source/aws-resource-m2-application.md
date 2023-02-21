# AWS::M2::Application<a name="aws-resource-m2-application"></a>

Specifies a new application with given parameters\. Requires an existing runtime environment and application definition file\.

For information about application definitions, see the [AWS Mainframe Modernization User Guide](https://docs.aws.amazon.com/m2/latest/userguide/applications-m2-definition.html)\.

## Syntax<a name="aws-resource-m2-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-m2-application-syntax.json"></a>

```
{
  "Type" : "AWS::M2::Application",
  "Properties" : {
      "[Definition](#cfn-m2-application-definition)" : Definition,
      "[Description](#cfn-m2-application-description)" : String,
      "[EngineType](#cfn-m2-application-enginetype)" : String,
      "[KmsKeyId](#cfn-m2-application-kmskeyid)" : String,
      "[Name](#cfn-m2-application-name)" : String,
      "[Tags](#cfn-m2-application-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-m2-application-syntax.yaml"></a>

```
Type: AWS::M2::Application
Properties: 
  [Definition](#cfn-m2-application-definition): 
    Definition
  [Description](#cfn-m2-application-description): String
  [EngineType](#cfn-m2-application-enginetype): String
  [KmsKeyId](#cfn-m2-application-kmskeyid): String
  [Name](#cfn-m2-application-name): String
  [Tags](#cfn-m2-application-tags): 
    Key : Value
```

## Properties<a name="aws-resource-m2-application-properties"></a>

`Definition`  <a name="cfn-m2-application-definition"></a>
The application definition for a particular application\. You can specify either inline JSON or an Amazon S3 bucket location\.  
For information about application definitions, see the [AWS Mainframe Modernization User Guide](https://docs.aws.amazon.com/m2/latest/userguide/applications-m2-definition.html)\.  
*Required*: Yes  
*Type*: [Definition](aws-properties-m2-application-definition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-m2-application-description"></a>
The description of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineType`  <a name="cfn-m2-application-enginetype"></a>
The type of the target platform for this application\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `bluage | microfocus`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-m2-application-kmskeyid"></a>
The identifier of a customer managed key\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-m2-application-name"></a>
The name of the application\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[A-Za-z0-9][A-Za-z0-9_\-]{1,59}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-m2-application-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-m2-application-return-values"></a>

### Ref<a name="aws-resource-m2-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the application Amazon Resource Name \(ARN\), such as the following:

 `{ "Ref": “SampleApp” }` 

Returns a value similar to the following:

 `arn:aws:m2:us-west-2:1234567890:app/y3ca6bhaife2bcvxar3lpivfou` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-m2-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-m2-application-return-values-fn--getatt-fn--getatt"></a>

`ApplicationArn`  <a name="ApplicationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the application\.

`ApplicationId`  <a name="ApplicationId-fn::getatt"></a>
The identifier of the application\.