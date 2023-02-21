# AWS::ImageBuilder::Component<a name="aws-resource-imagebuilder-component"></a>

Creates a new component that can be used to build, validate, test, and assess your image\. The component is based on a YAML document that you specify using exactly one of the following methods:
+ Inline, using the `data` property in the request body\.
+ A URL that points to a YAML document file stored in Amazon S3, using the `uri` property in the request body\.

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
      "[SupportedOsVersions](#cfn-imagebuilder-component-supportedosversions)" : [ String, ... ],
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
  [SupportedOsVersions](#cfn-imagebuilder-component-supportedosversions): 
    - String
  [Tags](#cfn-imagebuilder-component-tags): 
    Key : Value
  [Uri](#cfn-imagebuilder-component-uri): String
  [Version](#cfn-imagebuilder-component-version): String
```

## Properties<a name="aws-resource-imagebuilder-component-properties"></a>

`ChangeDescription`  <a name="cfn-imagebuilder-component-changedescription"></a>
The change description of the component\. Describes what change has been made in this version, or what makes this version different from other versions of this component\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Data`  <a name="cfn-imagebuilder-component-data"></a>
Component `data` contains inline YAML document content for the component\. Alternatively, you can specify the `uri` of a YAML document file stored in Amazon S3\. However, you cannot specify both properties\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16000`  
*Pattern*: `[^\x00]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-imagebuilder-component-description"></a>
Describes the contents of the component\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-imagebuilder-component-kmskeyid"></a>
The ID of the KMS key that is used to encrypt this component\.  
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
The operating system platform of the component\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Linux | Windows`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SupportedOsVersions`  <a name="cfn-imagebuilder-component-supportedosversions"></a>
 The operating system \(OS\) version supported by the component\. If the OS information is available, a prefix match is performed against the base image OS version during image recipe creation\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `25`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-imagebuilder-component-tags"></a>
The tags that apply to the component\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Uri`  <a name="cfn-imagebuilder-component-uri"></a>
The `uri` of a YAML component document file\. This must be an S3 URL \(`s3://bucket/key`\), and the requester must have permission to access the S3 bucket it points to\. If you use Amazon S3, you can specify component content up to your service quota\.  
Alternatively, you can specify the YAML document inline, using the component `data` property\. You cannot specify both properties\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-imagebuilder-component-version"></a>
The component version\. For example, `1.0.0`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-imagebuilder-component-return-values"></a>

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

`Name`  <a name="Name-fn::getatt"></a>
Returns the name of the component\.

`Type`  <a name="Type-fn::getatt"></a>
Image Builder determines the component type based on the phases that are defined in the component document\. If there is only one phase, and its name is "test", then the type is `TEST`\. For all other components, the type is `BUILD`\.

## Examples<a name="aws-resource-imagebuilder-component--examples"></a>



### Create a component using Data<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_Data_"></a>

The following example shows the schema for the Component resource document in both JSON and YAML format\. This example includes details for the `Data` field \. You can use either the `Data` or `Uri` fields to reference the component document\.

#### JSON<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_Data_--json"></a>

```
{
	"Resources": {
		"ComponentAllParameters": {
			"Type": "AWS::ImageBuilder::Component",
			"Properties": {
				"Name": "component-name",
				"Platform": "Linux",
				"Version": "1.0.0",
				"Description": "description",
				"ChangeDescription": "change-description",
				"KmsKeyId": "customer-kms-key-id",
				"SupportedOsVersions": ["Amazon Linux 2"],
				"Tags": {
					"CustomerComponentTagKey1": "CustomerComponentTagValue1",
					"CustomerComponentTagKey2": "CustomerComponentTagValue2"
				},
				"Data": "name: HelloWorldTestingLinuxDoc - InlineData\n description: This is hello world testing doc\nschemaVersion: 1.0\n\nphases:\n  - name: build\n    steps:\n      - name: HelloWorldStep\n        action: ExecuteBash\n        inputs:\n          commands:\n            - echo \"Hello World! Build.\"\n  - name: validate\n    steps:\n      - name: HelloWorldStep\n        action: ExecuteBash\n        inputs:\n          commands:\n            - echo \"Hello World! Validate.\"\n  - name: test\n    steps:\n      - name: HelloWorldStep\n        action: ExecuteBash\n        inputs:\n          commands:\n            - echo \"Hello World! Test.\"\n"
			}
		}
	}
}
```

#### YAML<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_Data_--yaml"></a>

```
Resources:
  ComponentAllParameters:
    Type: 'AWS::ImageBuilder::Component'
    Properties:
      Name: 'component-name'
      Platform: 'Linux'
      Version: '1.0.0'
      Description: 'description'
      ChangeDescription: 'change-description'
      KmsKeyId: 'customer-kms-key-id'
      SupportedOsVersions: 
        - 'Amazon Linux 2'
      Tags:
        CustomerComponentTagKey1: 'CustomerComponentTagValue1'
        CustomerComponentTagKey2: 'CustomerComponentTagValue2'
      # Require one of 'Data' or 'Uri' for Component template
      Data: |
        name: HelloWorldTestingLinuxDoc - InlineData
        description: This is hello world testing doc
        schemaVersion: 1.0

        phases:
          - name: build
            steps:
              - name: HelloWorldStep
                action: ExecuteBash
                inputs:
                  commands:
                    - echo "Hello World! Build."
          - name: validate
            steps:
              - name: HelloWorldStep
                action: ExecuteBash
                inputs:
                  commands:
                    - echo "Hello World! Validate."
          - name: test
            steps:
              - name: HelloWorldStep
                action: ExecuteBash
                inputs:
                  commands:
                    - echo "Hello World! Test."
```

### Create a component using a Uri<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_a_Uri"></a>

The following example shows the schema for the Component resource document in both YAML and JSON format\. This example includes details for the `Uri` field \. You can use either the `Data` or `Uri` fields to reference the component document\.

#### YAML<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_a_Uri--yaml"></a>

```
Resources:
  ComponentAllParameters:
    Type: 'AWS::ImageBuilder::Component'
    Properties:
      Name: 'component-name'
      Platform: 'Linux'
      Version: '1.0.0'
      # Require one of 'Data' or 'Uri' for Component template
      Uri: 's3://imagebuilder/component_document.yml'
      Description: 'description'
      ChangeDescription: 'change-description'
      KmsKeyId: 'customer-kms-key-id'
      SupportedOsVersions: 
      - 'CentOS'
      - 'Red Hat Enterprise Linux'
      Tags:
        CustomerComponentTagKey1: 'CustomerComponentTagValue1'
        CustomerComponentTagKey2: 'CustomerComponentTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-component--examples--Create_a_component_using_a_Uri--json"></a>

```
{
    "Resources": {
        "ComponentAllParameters": {
            "Type": "AWS::ImageBuilder::Component",
            "Properties": {
                "Name": "component-name",
                "Platform": "Linux",
                "Version": "1.0.0",
                "Uri": "s3://imagebuilder/component_document.yml",
                "Description": "description",
                "ChangeDescription": "change-description",
                "KmsKeyId": "customer-kms-key-id",
                "SupportedOsVersions": ["CentOS", "Red Hat Enterprise Linux"],
                "Tags": {
                    "CustomerComponentTagKey1": "CustomerComponentTagValue1",
                    "CustomerComponentTagKey2": "CustomerComponentTagValue2"
                }
            }
        }
    }
}
```