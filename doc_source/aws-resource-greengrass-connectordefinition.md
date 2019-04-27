# AWS::Greengrass::ConnectorDefinition<a name="aws-resource-greengrass-connectordefinition"></a>

The `AWS::Greengrass::ConnectorDefinition` resource represents a connector definition for AWS IoT Greengrass\. Connector definitions are used to organize your connector definition versions\.

Connector definitions can reference multiple connector definition versions\.

![\[A connector definition hierarchy with associated connector definition versions and connectors.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-connector.png)

All connector definition versions must be associated with a connector definition\. Each connector definition version can contain one or more connectors\.

**Note**  
When you create a connector definition, you can optionally include an initial connector definition version\. To associate a connector definition version later, create an [AWS::Greengrass::ConnectorDefinitionVersion](aws-resource-greengrass-connectordefinitionversion.md) resource and specify the ID of this connector definition\.  
After you create the connector definition version that contains the connectors you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-connectordefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-connectordefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ConnectorDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-connectordefinition-initialversion)" : [*ConnectorDefinitionVersion*](aws-properties-greengrass-connectordefinition-connectordefinitionversion.md),
    "[Name](#cfn-greengrass-connectordefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-connectordefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::ConnectorDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-connectordefinition-initialversion): 
    [*ConnectorDefinitionVersion*](aws-properties-greengrass-connectordefinition-connectordefinitionversion.md)
  [Name](#cfn-greengrass-connectordefinition-name): String
```

## Properties<a name="aws-resource-greengrass-connectordefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-connectordefinition-initialversion"></a>
The connector definition version to include when the connector definition is created\. A connector definition version contains a list of [`connector`](aws-properties-greengrass-connectordefinition-connector.md) property types\.  
To associate a connector definition version after the connector definition is created, create an [AWS::Greengrass::ConnectorDefinitionVersion](aws-resource-greengrass-connectordefinitionversion.md) resource and specify the ID of this connector definition\.
 *Required*: No  
 *Type*: [ConnectorDefinitionVersion](aws-properties-greengrass-connectordefinition-connectordefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-connectordefinition-name"></a>
The name of the connector definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-connectordefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-connectordefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::ConnectorDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the connector definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-connectordefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `ConnectorDefinitionVersion` that was added to the `ConnectorDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `ConnectorDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `ConnectorDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `ConnectorDefinition`, such as `MyConnectorDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-connectordefinition-examples"></a>

### Connector Definition Snippet<a name="aws-resource-greengrass-connectordefinition-example1"></a>

The following snippet defines a connector definition resource with an initial version that contains a connector\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-connectordefinition-example1.json"></a>

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

#### YAML<a name="aws-resource-greengrass-connectordefinition-example1.yaml"></a>

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

## See Also<a name="aws-resource-greengrass-connectordefinition-seealso"></a>
+ [CreateConnectorDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createconnectordefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)