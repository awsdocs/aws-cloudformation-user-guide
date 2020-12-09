# AWS::Glue::Connection PhysicalConnectionRequirements<a name="aws-properties-glue-connection-physicalconnectionrequirements"></a>

Specifies the physical requirements for a connection\.

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

`AvailabilityZone`  <a name="cfn-glue-connection-physicalconnectionrequirements-availabilityzone"></a>
The connection's Availability Zone\. This field is redundant because the specified subnet implies the Availability Zone to be used\. Currently the field must be populated, but it will be deprecated in the future\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIdList`  <a name="cfn-glue-connection-physicalconnectionrequirements-securitygroupidlist"></a>
The security group ID list used by the connection\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-glue-connection-physicalconnectionrequirements-subnetid"></a>
The subnet ID used by the connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)