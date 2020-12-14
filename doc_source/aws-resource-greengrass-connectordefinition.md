# AWS::Greengrass::ConnectorDefinition<a name="aws-resource-greengrass-connectordefinition"></a>

The `AWS::Greengrass::ConnectorDefinition` resource represents a connector definition for AWS IoT Greengrass\. Connector definitions are used to organize your connector definition versions\.

Connector definitions can reference multiple connector definition versions\. All connector definition versions must be associated with a connector definition\. Each connector definition version can contain one or more connectors\.

**Note**  
When you create a connector definition, you can optionally include an initial connector definition version\. To associate a connector definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html) resource and specify the ID of this connector definition\.  
After you create the connector definition version that contains the connectors you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-connectordefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-connectordefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ConnectorDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-connectordefinition-initialversion)" : ConnectorDefinitionVersion,
      "[Name](#cfn-greengrass-connectordefinition-name)" : String,
      "[Tags](#cfn-greengrass-connectordefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-connectordefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::ConnectorDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-connectordefinition-initialversion): 
    ConnectorDefinitionVersion
  [Name](#cfn-greengrass-connectordefinition-name): String
  [Tags](#cfn-greengrass-connectordefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-connectordefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-connectordefinition-initialversion"></a>
The connector definition version to include when the connector definition is created\. A connector definition version contains a list of [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-connectordefinition-connector.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-connectordefinition-connector.html) property types\.  
To associate a connector definition version after the connector definition is created, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html) resource and specify the ID of this connector definition\.
*Required*: No  
*Type*: [ConnectorDefinitionVersion](aws-properties-greengrass-connectordefinition-connectordefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-connectordefinition-name"></a>
The name of the connector definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-connectordefinition-tags"></a>
Application\-specific metadata to attach to the connector definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
This `Json` property type is processed as a map of key\-value pairs\. It uses the following format, which is different from most `Tags` implementations in AWS CloudFormation templates\.  

```
"Tags": {
    "KeyName0": "value",
    "KeyName1": "value",
    "KeyName2": "value"
}
```
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-greengrass-connectordefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-connectordefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the connector definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-connectordefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-connectordefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `ConnectorDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `ConnectorDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `ConnectorDefinitionVersion` that was added to the `ConnectorDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `ConnectorDefinition`, such as `MyConnectorDefinition`\. 

## Examples<a name="aws-resource-greengrass-connectordefinition--examples"></a>



### Connector Definition Snippet<a name="aws-resource-greengrass-connectordefinition--examples--Connector_Definition_Snippet"></a>

The following snippet defines a connector definition resource with an initial version that contains a connector\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) resource\.

#### JSON<a name="aws-resource-greengrass-connectordefinition--examples--Connector_Definition_Snippet--json"></a>

```
"TestConnectorDefinition": {
    "Type": "AWS::Greengrass::ConnectorDefinition",
    "Properties": {
        "Name": "DemoTestConnectorDefinition",
        "InitialVersion": {
            "Connectors": [
                {
                    "Id": "Connector1",
                    "ConnectorArn": {
                        "Fn::Join": [
                            ":",
                            [
                                "arn:aws:greengrass",
                                {
                                    "Ref": "AWS::Region"
                                },
                                ":/connectors/SNS/versions/1"
                            ]
                        ]
                    },
                    "Parameters": {
                        "DefaultSNSArn": {
                            "Fn::Join": [
                                ":",
                                [
                                    "arn:aws:sns",
                                    {
                                        "Ref": "AWS::Region"
                                    },
                                    {
                                        "Ref": "AWS::AccountId"
                                    },
                                    "defaultSns"
                                ]
                            ]
                        }
                    }
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-greengrass-connectordefinition--examples--Connector_Definition_Snippet--yaml"></a>

```
TestConnectorDefinition:
  Type: 'AWS::Greengrass::ConnectorDefinition'
  Properties:
    Name: DemoTestConnectorDefinition
    InitialVersion:
      Connectors:
        - Id: Connector1
          ConnectorArn: !Join 
            - ':'
            - - 'arn:aws:greengrass'
              - !Ref 'AWS::Region'
              - ':/connectors/SNS/versions/1'
          Parameters:
            DefaultSNSArn: !Join 
              - ':'
              - - 'arn:aws:sns'
                - !Ref 'AWS::Region'
                - !Ref 'AWS::AccountId'
                - defaultSns
```

## See also<a name="aws-resource-greengrass-connectordefinition--seealso"></a>
+  [CreateConnectorDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createconnectordefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 