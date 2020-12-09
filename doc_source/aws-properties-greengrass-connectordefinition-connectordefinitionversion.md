# AWS::Greengrass::ConnectorDefinition ConnectorDefinitionVersion<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion"></a>

<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-description"></a>A connector definition version contains a list of connectors\.

**Note**  
After you create a connector definition version that contains the connectors you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-inheritance"></a> In an AWS CloudFormation template, `ConnectorDefinitionVersion` is the property type of the `InitialVersion` property in the [ `AWS::Greengrass::ConnectorDefinition` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html) resource\.

## Syntax<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-syntax.json"></a>

```
{
  "[Connectors](#cfn-greengrass-connectordefinition-connectordefinitionversion-connectors)" : [ Connector, ... ]
}
```

### YAML<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-syntax.yaml"></a>

```
  [Connectors](#cfn-greengrass-connectordefinition-connectordefinitionversion-connectors): 
    - Connector
```

## Properties<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion-properties"></a>

`Connectors`  <a name="cfn-greengrass-connectordefinition-connectordefinitionversion-connectors"></a>
The connectors in this version\. Only one instance of a given connector can be added to a connector definition version at a time\.  
*Required*: Yes  
*Type*: List of [Connector](aws-properties-greengrass-connectordefinition-connector.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-connectordefinition-connectordefinitionversion--seealso"></a>
+  [ConnectorDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-connectordefinitionversion.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 