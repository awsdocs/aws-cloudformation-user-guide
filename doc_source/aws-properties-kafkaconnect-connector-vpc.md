# AWS::KafkaConnect::Connector Vpc<a name="aws-properties-kafkaconnect-connector-vpc"></a>

Information about the VPC in which the connector resides\.

## Syntax<a name="aws-properties-kafkaconnect-connector-vpc-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-vpc-syntax.json"></a>

```
{
  "[SecurityGroups](#cfn-kafkaconnect-connector-vpc-securitygroups)" : [ String, ... ],
  "[Subnets](#cfn-kafkaconnect-connector-vpc-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-vpc-syntax.yaml"></a>

```
  [SecurityGroups](#cfn-kafkaconnect-connector-vpc-securitygroups): 
    - String
  [Subnets](#cfn-kafkaconnect-connector-vpc-subnets): 
    - String
```

## Properties<a name="aws-properties-kafkaconnect-connector-vpc-properties"></a>

`SecurityGroups`  <a name="cfn-kafkaconnect-connector-vpc-securitygroups"></a>
The security groups for the connector\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-kafkaconnect-connector-vpc-subnets"></a>
The subnets for the connector\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)