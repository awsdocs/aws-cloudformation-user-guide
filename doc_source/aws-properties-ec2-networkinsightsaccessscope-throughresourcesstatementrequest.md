# AWS::EC2::NetworkInsightsAccessScope ThroughResourcesStatementRequest<a name="aws-properties-ec2-networkinsightsaccessscope-throughresourcesstatementrequest"></a>

Describes a through resource statement\.

## Syntax<a name="aws-properties-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-syntax.json"></a>

```
{
  "[ResourceStatement](#cfn-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-resourcestatement)" : ResourceStatementRequest
}
```

### YAML<a name="aws-properties-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-syntax.yaml"></a>

```
  [ResourceStatement](#cfn-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-resourcestatement): 
    ResourceStatementRequest
```

## Properties<a name="aws-properties-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-properties"></a>

`ResourceStatement`  <a name="cfn-ec2-networkinsightsaccessscope-throughresourcesstatementrequest-resourcestatement"></a>
The resource statement\.  
*Required*: No  
*Type*: [ResourceStatementRequest](aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)