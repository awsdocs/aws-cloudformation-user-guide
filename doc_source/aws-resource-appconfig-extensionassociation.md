# AWS::AppConfig::ExtensionAssociation<a name="aws-resource-appconfig-extensionassociation"></a>

When you create an extension or configure an AWS authored extension, you associate the extension with an AWS AppConfig application, environment, or configuration profile\. For example, you can choose to run the ` AWS AppConfig deployment events to Amazon SNS` AWS authored extension and receive notifications on an Amazon SNS topic anytime a configuration deployment is started for a specific application\. Defining which extension to associate with an AWS AppConfig resource is called an *extension association*\. An extension association is a specified relationship between an extension and an AWS AppConfig resource, such as an application or a configuration profile\. For more information about extensions and associations, see [Working with AWS AppConfig extensions](https://docs.aws.amazon.com/appconfig/latest/userguide/working-with-appconfig-extensions.html) in the * AWS AppConfig User Guide*\.

## Syntax<a name="aws-resource-appconfig-extensionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-extensionassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::ExtensionAssociation",
  "Properties" : {
      "[ExtensionIdentifier](#cfn-appconfig-extensionassociation-extensionidentifier)" : String,
      "[ExtensionVersionNumber](#cfn-appconfig-extensionassociation-extensionversionnumber)" : Integer,
      "[Parameters](#cfn-appconfig-extensionassociation-parameters)" : {Key : Value, ...},
      "[ResourceIdentifier](#cfn-appconfig-extensionassociation-resourceidentifier)" : String,
      "[Tags](#cfn-appconfig-extensionassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-extensionassociation-syntax.yaml"></a>

```
Type: AWS::AppConfig::ExtensionAssociation
Properties: 
  [ExtensionIdentifier](#cfn-appconfig-extensionassociation-extensionidentifier): String
  [ExtensionVersionNumber](#cfn-appconfig-extensionassociation-extensionversionnumber): Integer
  [Parameters](#cfn-appconfig-extensionassociation-parameters): 
    Key : Value
  [ResourceIdentifier](#cfn-appconfig-extensionassociation-resourceidentifier): String
  [Tags](#cfn-appconfig-extensionassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-appconfig-extensionassociation-properties"></a>

`ExtensionIdentifier`  <a name="cfn-appconfig-extensionassociation-extensionidentifier"></a>
The name, the ID, or the Amazon Resource Name \(ARN\) of the extension\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExtensionVersionNumber`  <a name="cfn-appconfig-extensionassociation-extensionversionnumber"></a>
The version number of the extension\. If not specified, AWS AppConfig uses the maximum version of the extension\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-appconfig-extensionassociation-parameters"></a>
The parameter names and values defined in the extensions\. Extension parameters marked `Required` must be entered for this field\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceIdentifier`  <a name="cfn-appconfig-extensionassociation-resourceidentifier"></a>
The ARN of an application, configuration profile, or environment\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appconfig-extensionassociation-tags"></a>
Adds one or more tags for the specified extension association\. Tags are metadata that help you categorize resources in different ways, for example, by purpose, owner, or environment\. Each tag consists of a key and an optional value, both of which you define\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appconfig-extensionassociation-return-values"></a>

### Ref<a name="aws-resource-appconfig-extensionassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns information about the extension association\.

### Fn::GetAtt<a name="aws-resource-appconfig-extensionassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appconfig-extensionassociation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the extension defined in the association\.

`ExtensionArn`  <a name="ExtensionArn-fn::getatt"></a>
The ARN of the extension defined in the association\.

`Id`  <a name="Id-fn::getatt"></a>
The system\-generated ID for the association\.

`ResourceArn`  <a name="ResourceArn-fn::getatt"></a>
The ARNs of applications, configuration profiles, or environments defined in the association\.

## Examples<a name="aws-resource-appconfig-extensionassociation--examples"></a>



### AWS AppConfig create extension association example<a name="aws-resource-appconfig-extensionassociation--examples--_create_extension_association_example"></a>

An extension association defines which extension to associate with an AWS AppConfig resource\. An extension association is a specified relationship between an extension and an AWS AppConfig resource, such as an application or a configuration profile\. The following example creates an extension association between an application called MyDependentApplication and an extension called MyAmazingExtension

#### JSON<a name="aws-resource-appconfig-extensionassociation--examples--_create_extension_association_example--json"></a>

```
{
  "Resources": {
    "BasicExtensionAssociation": {
      "Type": "AWS::AppConfig::ExtensionAssociation",
      "Properties": {
        "ExtensionIdentifier": "MyAmazingExtension",
        "ExtensionVersionNumber": 0,
        "ResourceIdentifier": [
          "/",
          [
            "arn:${AWS::Partition}:appconfig:${AWS::Region}:${AWS::AccountId}:application",
            "MyApplication"
          ]
        ],
        "Parameters": {
          "MyTestParam": "My test parameter value"
        },
        "Tags": [
          {
            "Key": "ExtAssociation",
            "Value": "Test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-extensionassociation--examples--_create_extension_association_example--yaml"></a>

```
Resources:
  BasicExtensionAssociation:
    Type: AWS::AppConfig::ExtensionAssociation
    Properties:
      ExtensionIdentifier: !ImportValue MyAmazingExtension
      ExtensionVersionNumber: 0
      ResourceIdentifier: !Join
        - '/'
        - - !Sub 'arn:${AWS::Partition}:appconfig:${AWS::Region}:${AWS::AccountId}:application'
          - !ImportValue MyApplication
      Parameters:
        MyTestParam: "My test parameter value"
      Tags:
        - Key: ExtAssociation
          Value: Test
```

## See also<a name="aws-resource-appconfig-extensionassociation--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) 
+  [Working with AWS AppConfig extensions](https://docs.aws.amazon.com/appconfig/latest/userguide/working-with-appconfig-extensions.html)