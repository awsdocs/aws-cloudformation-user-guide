# AWS::AppConfig::Extension<a name="aws-resource-appconfig-extension"></a>

Creates an AWS AppConfig extension\. An extension augments your ability to inject logic or behavior at different points during the AWS AppConfig workflow of creating or deploying a configuration\.

You can create your own extensions or use the AWS authored extensions provided by AWS AppConfig\. For an AWS AppConfig extension that uses AWS Lambda, you must create a Lambda function to perform any computation and processing defined in the extension\. If you plan to create custom versions of the AWS authored notification extensions, you only need to specify an Amazon Resource Name \(ARN\) in the `Uri` field for the new extension version\.
+ For a custom EventBridge notification extension, enter the ARN of the EventBridge default events in the `Uri` field\.
+ For a custom Amazon SNS notification extension, enter the ARN of an Amazon SNS topic in the `Uri` field\.
+ For a custom Amazon SQS notification extension, enter the ARN of an Amazon SQS message queue in the `Uri` field\. 

For more information about extensions, see [Working with AWS AppConfig extensions](https://docs.aws.amazon.com/appconfig/latest/userguide/working-with-appconfig-extensions.html) in the * AWS AppConfig User Guide*\.

## Syntax<a name="aws-resource-appconfig-extension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-extension-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::Extension",
  "Properties" : {
      "[Actions](#cfn-appconfig-extension-actions)" : Json,
      "[Description](#cfn-appconfig-extension-description)" : String,
      "[LatestVersionNumber](#cfn-appconfig-extension-latestversionnumber)" : Integer,
      "[Name](#cfn-appconfig-extension-name)" : String,
      "[Parameters](#cfn-appconfig-extension-parameters)" : {Key: Value, ...},
      "[Tags](#cfn-appconfig-extension-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-extension-syntax.yaml"></a>

```
Type: AWS::AppConfig::Extension
Properties: 
  [Actions](#cfn-appconfig-extension-actions): Json
  [Description](#cfn-appconfig-extension-description): String
  [LatestVersionNumber](#cfn-appconfig-extension-latestversionnumber): Integer
  [Name](#cfn-appconfig-extension-name): String
  [Parameters](#cfn-appconfig-extension-parameters): 
    Key: Value
  [Tags](#cfn-appconfig-extension-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-appconfig-extension-properties"></a>

`Actions`  <a name="cfn-appconfig-extension-actions"></a>
The actions defined in the extension\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appconfig-extension-description"></a>
Information about the extension\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LatestVersionNumber`  <a name="cfn-appconfig-extension-latestversionnumber"></a>
You can omit this field when you create an extension\. When you create a new version, specify the most recent current version number\. For example, you create version 3, enter 2 for this field\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appconfig-extension-name"></a>
A name for the extension\. Each extension name in your account must be unique\. Extension versions use the same name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-appconfig-extension-parameters"></a>
The parameters accepted by the extension\. You specify parameter values when you associate the extension to an AWS AppConfig resource by using the `CreateExtensionAssociation` API action\. For AWS Lambda extension actions, these parameters are included in the Lambda request object\.  
*Required*: No  
*Type*: Map of [Parameter](aws-properties-appconfig-extension-parameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appconfig-extension-tags"></a>
Adds one or more tags for the specified extension\. Tags are metadata that help you categorize resources in different ways, for example, by purpose, owner, or environment\. Each tag consists of a key and an optional value, both of which you define\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appconfig-extension-return-values"></a>

### Ref<a name="aws-resource-appconfig-extension-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns information about the extension\.

### Fn::GetAtt<a name="aws-resource-appconfig-extension-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appconfig-extension-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The system\-generated Amazon Resource Name \(ARN\) for the extension\.

`Id`  <a name="Id-fn::getatt"></a>
The system\-generated ID of the extension\.

`VersionNumber`  <a name="VersionNumber-fn::getatt"></a>
The extension version number\.

## Examples<a name="aws-resource-appconfig-extension--examples"></a>



### AWS AppConfig create extension example<a name="aws-resource-appconfig-extension--examples--_create_extension_example"></a>

An extension augments your ability to inject logic or behavior at different points during the AWS AppConfig workflow of creating or deploying a configuration\. You can create your own extensions or use the AWS authored extensions provided by AWS AppConfig\. The following extension performs an action using AWS Lambda \(as defined by the `Uri` field\) before a configuration version is created by AWS AppConfig \(as defined by the `PRE_CREATE_HOSTED_CONFIGURATION_VERSION` action point\)\.

#### JSON<a name="aws-resource-appconfig-extension--examples--_create_extension_example--json"></a>

```
{
  "Resources": {
    "BasicExtension": {
      "Type": "AWS::AppConfig::Extension",
      "Properties": {
        "Name": "My Test Extension",
        "Description": "My test extension",
        "LatestVersionNumber": 0,
        "Actions": {
          "PRE_CREATE_HOSTED_CONFIGURATION_VERSION": [
            {
              "Name": "My Test Action",
              "Uri": "DependentLambda.Arn",
              "RoleArn": "DependentRole.Arn",
              "Description": "My test action point"
            }
          ]
        },
        "Parameters": {
          "MyTestParam": {
            "Required": false,
            "Description": "My test parameter"
          }
        },
        "Tags": [
          {
            "Key": "Ext",
            "Value": "Test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-extension--examples--_create_extension_example--yaml"></a>

```
Resources:
  BasicExtension:
    Type: AWS::AppConfig::Extension
    Properties:
      Name: "My Test Extension"
      Description: "My test extension"
      LatestVersionNumber: 0
      Actions:
        PRE_CREATE_HOSTED_CONFIGURATION_VERSION:
          - Name: "My Test Action"
            Uri: !GetAtt DependentLambda.Arn
            RoleArn: !GetAtt DependentRole.Arn
            Description: "My test action point"
      Parameters:
        MyTestParam:
          Required: false
          Description: "My test parameter"
      Tags:
        - Key: Ext
          Value: Test
```

## See also<a name="aws-resource-appconfig-extension--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) 
+  [Working with AWS AppConfig extensions](https://docs.aws.amazon.com/appconfig/latest/userguide/working-with-appconfig-extensions.html)