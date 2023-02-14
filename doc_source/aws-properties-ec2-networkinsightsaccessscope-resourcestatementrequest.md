# AWS::EC2::NetworkInsightsAccessScope ResourceStatementRequest<a name="aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest"></a>

Describes a resource statement\.

## Syntax<a name="aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest-syntax.json"></a>

```
{
  "[Resources](#cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resources)" : [ String, ... ],
  "[ResourceTypes](#cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resourcetypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest-syntax.yaml"></a>

```
  [Resources](#cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resources): 
    - String
  [ResourceTypes](#cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resourcetypes): 
    - String
```

## Properties<a name="aws-properties-ec2-networkinsightsaccessscope-resourcestatementrequest-properties"></a>

`Resources`  <a name="cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resources"></a>
The resources\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceTypes`  <a name="cfn-ec2-networkinsightsaccessscope-resourcestatementrequest-resourcetypes"></a>
The resource types\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)