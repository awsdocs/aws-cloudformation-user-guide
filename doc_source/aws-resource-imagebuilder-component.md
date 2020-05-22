# AWS::ImageBuilder::Component<a name="aws-resource-imagebuilder-component"></a>

Components are orchestration documents that define a sequence of steps for downloading, installing, and configuring software packages or for defining tests to run on software packages\. They also define validation and security hardening steps\. A component is defined using a YAML document format\. For more information, see [Using Documents in EC2 Image Builder](https://docs.aws.amazon.com/imagebuilder/latest/userguide/image-builder-application-documents.html)\.

## Syntax<a name="aws-resource-imagebuilder-component-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-component-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::Component",
  "Properties" : {
      "[ChangeDescription](#cfn-imagebuilder-component-changedescription)" : String,
      "[Data](#cfn-imagebuilder-component-data)" : String,
      "[Description](#cfn-imagebuilder-component-description)" : String,
      "[KmsKeyId](#cfn-imagebuilder-component-kmskeyid)" : String,
      "[Name](#cfn-imagebuilder-component-name)" : String,
      "[Platform](#cfn-imagebuilder-component-platform)" : String,
      "[Tags](#cfn-imagebuilder-component-tags)" : {Key : Value, ...},
      "[Uri](#cfn-imagebuilder-component-uri)" : String,
      "[Version](#cfn-imagebuilder-component-version)" : String
    }
}
```

### YAML<a name="aws-resource-imagebuilder-component-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::Component
Properties: 
  [ChangeDescription](#cfn-imagebuilder-component-changedescription): String
  [Data](#cfn-imagebuilder-component-data): String
  [Description](#cfn-imagebuilder-component-description): String
  [KmsKeyId](#cfn-imagebuilder-component-kmskeyid): String
  [Name](#cfn-imagebuilder-component-name): String
  [Platform](#cfn-imagebuilder-component-platform): String
  [Tags](#cfn-imagebuilder-component-tags): 
    Key : Value
  [Uri](#cfn-imagebuilder-component-uri): String
  [Version](#cfn-imagebuilder-component-version): String
```

## Properties<a name="aws-resource-imagebuilder-component-properties"></a>

`ChangeDescription`  <a name="cfn-imagebuilder-component-changedescription"></a>
A change description of the component\. For example `initial version`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Data`  <a name="cfn-imagebuilder-component-data"></a>
The data of the component\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-imagebuilder-component-description"></a>
The description of the component\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-imagebuilder-component-kmskeyid"></a>
The KMS key identifier used to encrypt the component\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-imagebuilder-component-name"></a>
The name of the component\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Platform`  <a name="cfn-imagebuilder-component-platform"></a>
The platform of the component\. For example, `Windows`\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `Linux | Windows`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-component-tags"></a>
The tags associated with the component\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Uri`  <a name="cfn-imagebuilder-component-uri"></a>
The URI of the component document\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-imagebuilder-component-version"></a>
The component version\. For example, `1.0.0`\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[0-9]+\.[0-9]+\.[0-9]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-imagebuilder-component-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-component-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-west-2:123456789012:component/examplecomponent/2019.12.02/1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-component-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-component-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the component\. The following pattern is applied: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`\.

`Encrypted`  <a name="Encrypted-fn::getatt"></a>
Returns the encryption status of the component\. For example `true` or `false`\.

`Type`  <a name="Type-fn::getatt"></a>
Returns the component type\. For example, `BUILD` or `TEST`\.

## Examples<a name="aws-resource-imagebuilder-component--examples"></a>

### Component creation with Data field details<a name="aws-resource-imagebuilder-component--examples--Component_creation_with_Data_field_details"></a>

The following example shows the component creation document in both YAML and JSON format with details for the `Data` field \. You can use either the`Data` or `Uri` fields to reference the component document\.

#### YAML<a name="aws-resource-imagebuilder-component--examples--Component_creation_with_Data_field_details--yaml"></a>

```
Type: AWS::ImageBuilder::Component
Properties: 
  ChangeDescription: String
  Description: String
  KmsKeyId: String
  Name: String
  Platform: String
  Tags: 
    Key : Value
  Version: String
  Data: |
    name: Python 3
    description: Install the latest version of Python 3.
    schemaVersion: 1.0
    phases:
      - name: build
        steps:
          - name: InstallPython3
            action: ExecuteBash
            inputs:
              commands:
                - sudo yum install python3 -y
```

#### JSON<a name="aws-resource-imagebuilder-component--examples--Component_creation_with_Data_field_details--json"></a>

```
{
    "Type": "AWS::ImageBuilder::Component",
    "Properties": {
        "ChangeDescription": "String",
        "Description": "String",
        "KmsKeyId": "String",
        "Name": "String",
        "Platform": "String",
        "Tags": {
            "Key": "Value"
        },
        "Version": "String",
        "Data": "name: Python 3\ndescription: Install the latest version of Python 3.\nschemaVersion: 1.0\nphases:\n  - name: build\n    steps:\n      - name: InstallPython3\n        action: ExecuteBash\n        inputs:\n          commands:\n            - sudo yum install python3 -y\n"
    }
}
```