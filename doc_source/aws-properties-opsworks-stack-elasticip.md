# AWS::OpsWorks::Stack ElasticIp<a name="aws-properties-opsworks-stack-elasticip"></a>

Describes an Elastic IP address\.

## Syntax<a name="aws-properties-opsworks-stack-elasticip-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-stack-elasticip-syntax.json"></a>

```
{
  "[Ip](#cfn-opsworks-stack-elasticip-ip)" : String,
  "[Name](#cfn-opsworks-stack-elasticip-name)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-elasticip-syntax.yaml"></a>

```
  [Ip](#cfn-opsworks-stack-elasticip-ip): String
  [Name](#cfn-opsworks-stack-elasticip-name): String
```

## Properties<a name="aws-properties-opsworks-stack-elasticip-properties"></a>

`Ip`  <a name="cfn-opsworks-stack-elasticip-ip"></a>
The IP address\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-opsworks-stack-elasticip-name"></a>
The name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)