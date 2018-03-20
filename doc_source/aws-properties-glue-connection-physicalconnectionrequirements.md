# AWS Glue Connection PhysicalConnectionRequirements<a name="aws-properties-glue-connection-physicalconnectionrequirements"></a>

<a name="aws-properties-glue-connection-physicalconnectionrequirements-description"></a>The `PhysicalConnectionRequirements` property type specifies the physical connection requirements that are needed to make an AWS Glue connection, such as VPC and SecurityGroup\.

<a name="aws-properties-glue-connection-physicalconnectionrequirements-inheritance"></a> `PhysicalConnectionRequirements` is a property of the [AWS Glue Connection ConnectionInput](aws-properties-glue-connection-connectioninput.md) property type\.

## Syntax<a name="aws-properties-glue-connection-physicalconnectionrequirements-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-connection-physicalconnectionrequirements-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-glue-connection-physicalconnectionrequirements-availabilityzone)" : String,
  "[SecurityGroupIdList](#cfn-glue-connection-physicalconnectionrequirements-securitygroupidlist)" : [ String, ... ],
  "[SubnetId](#cfn-glue-connection-physicalconnectionrequirements-subnetid)" : String
}
```

### YAML<a name="aws-properties-glue-connection-physicalconnectionrequirements-syntax.yaml"></a>

```
[AvailabilityZone](#cfn-glue-connection-physicalconnectionrequirements-availabilityzone): String
[SecurityGroupIdList](#cfn-glue-connection-physicalconnectionrequirements-securitygroupidlist): 
  - String
[SubnetId](#cfn-glue-connection-physicalconnectionrequirements-subnetid): String
```

## Properties<a name="aws-properties-glue-connection-physicalconnectionrequirements-properties"></a>

For more information, see [PhysicalConnectionRequirements Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-connections.html#aws-glue-api-catalog-connections-PhysicalConnectionRequirements) in the *AWS Glue Developer Guide*\.

`AvailabilityZone`  <a name="cfn-glue-connection-physicalconnectionrequirements-availabilityzone"></a>
The connection's Availability Zone\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIdList`  <a name="cfn-glue-connection-physicalconnectionrequirements-securitygroupidlist"></a>
A list of UTF\-8 strings that specify the security group IDs that are used by the connection\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetId`  <a name="cfn-glue-connection-physicalconnectionrequirements-subnetid"></a>
The subnet ID that's used by the connection\. It must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 