# AWS::EC2::NetworkInsightsAccessScope PathStatementRequest<a name="aws-properties-ec2-networkinsightsaccessscope-pathstatementrequest"></a>

Describes a path statement\.

## Syntax<a name="aws-properties-ec2-networkinsightsaccessscope-pathstatementrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsaccessscope-pathstatementrequest-syntax.json"></a>

```
{
  "[PacketHeaderStatement](#cfn-ec2-networkinsightsaccessscope-pathstatementrequest-packetheaderstatement)" : PacketHeaderStatementRequest,
  "[ResourceStatement](#cfn-ec2-networkinsightsaccessscope-pathstatementrequest-resourcestatement)" : ResourceStatementRequest
}
```

### YAML<a name="aws-properties-ec2-networkinsightsaccessscope-pathstatementrequest-syntax.yaml"></a>

```
  [PacketHeaderStatement](#cfn-ec2-networkinsightsaccessscope-pathstatementrequest-packetheaderstatement): 
    PacketHeaderStatementRequest
  [ResourceStatement](#cfn-ec2-networkinsightsaccessscope-pathstatementrequest-resourcestatement): 
    ResourceStatementRequest
```

## Properties<a name="aws-properties-ec2-networkinsightsaccessscope-pathstatementrequest-properties"></a>

`PacketHeaderStatement`  <a name="cfn-ec2-networkinsightsaccessscope-pathstatementrequest-packetheaderstatement"></a>
The packet header statement\.  
*Required*: No  
*Type*: [PacketHeaderStatementRequest](aws-properties-ec2-networkinsightsaccessscope-packetheaderstatementrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceStatement`  <a name="cfn-ec2-networkinsightsaccessscope-pathstatementrequest-resourcestatement"></a>
The resource statement\.  
*Required*: No  
*Type*: [ResourceStatementRequest](aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)