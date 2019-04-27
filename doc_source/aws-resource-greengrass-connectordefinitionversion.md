# AWS::Greengrass::ConnectorDefinitionVersion<a name="aws-resource-greengrass-connectordefinitionversion"></a>

The `AWS::Greengrass::ConnectorDefinitionVersion` resource represents a connector definition version for AWS IoT Greengrass\. A connector definition version contains a list of connectors\.

**Note**  
To create a connector definition version, you must specify the ID of the connector definition that you want to associate with the version\. For information about creating a connector definition, see [AWS::Greengrass::ConnectorDefinition](aws-resource-greengrass-connectordefinition.md)\.  
After you create a connector definition version that contains the connectors you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-connectordefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-connectordefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::ConnectorDefinitionVersion",
  "Properties" : {
    "[Connectors](#cfn-greengrass-connectordefinitionversion-connectors)" : [ [*Connector*](aws-properties-greengrass-connectordefinitionversion-connector.md), ... ],
    "[ConnectorDefinitionId](#cfn-greengrass-connectordefinitionversion-connectordefinitionid)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-connectordefinitionversion-syntax.yaml"></a>

```
Type: "AWS::Greengrass::ConnectorDefinitionVersion"
Properties:
  [Connectors](#cfn-greengrass-connectordefinitionversion-connectors): 
    - [*Connector*](aws-properties-greengrass-connectordefinitionversion-connector.md)
  [ConnectorDefinitionId](#cfn-greengrass-connectordefinitionversion-connectordefinitionid): String
```

## Properties<a name="aws-resource-greengrass-connectordefinitionversion-properties"></a>

`Connectors`  <a name="cfn-greengrass-connectordefinitionversion-connectors"></a>
The connectors in this version\. Only one instance of a given connector can be added to the connector definition version at a time\.  
 *Required*: Yes  
 *Type*: List of [Connector](aws-properties-greengrass-connectordefinitionversion-connector.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ConnectorDefinitionId`  <a name="cfn-greengrass-connectordefinitionversion-connectordefinitionid"></a>
The ID of the connector definition associated with this version\. This value is a GUID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-greengrass-connectordefinitionversion-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-connectordefinitionversion-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::ConnectorDefinitionVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the connector definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-greengrass-connectordefinitionversion-examples"></a>

### Connector Definition Version Snippet<a name="aws-resource-greengrass-connectordefinitionversion-example1"></a>

The following snippet defines connector definition and connector definition version resources\. The connector definition version references the connector definition and contains a connector\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-connectordefinitionversion-example1.json"></a>

```
"TestConnectorDefinition": {
    "Type": "AWS::Greengrass::ConnectorDefinition",
    "Properties": {
        "Name": "DemoTestConnectorDefinition"
    }
},
"TestConnectorDefinitionVersion": {
    "Type": "AWS::Greengrass::ConnectorDefinitionVersion",
    "Properties": {
        "ConnectorDefinitionId": {
            "Ref": "TestConnectorDefinition"
        },
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
```

#### YAML<a name="aws-resource-greengrass-connectordefinitionversion-example1.yaml"></a>

```
TestConnectorDefinition:
  Type: 'AWS::Greengrass::ConnectorDefinition'
  Properties:
    Name: DemoTestConnectorDefinition
TestConnectorDefinitionVersion:
  Type: 'AWS::Greengrass::ConnectorDefinitionVersion'
  Properties:
    ConnectorDefinitionId: !Ref TestConnectorDefinition
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

## See Also<a name="aws-resource-greengrass-connectordefinitionversion-seealso"></a>
+ [ConnectorDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-connectordefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)