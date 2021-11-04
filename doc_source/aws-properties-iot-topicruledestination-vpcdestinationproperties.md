# AWS::IoT::TopicRuleDestination VpcDestinationProperties<a name="aws-properties-iot-topicruledestination-vpcdestinationproperties"></a>

The properties of a virtual private cloud \(VPC\) destination\.

## Syntax<a name="aws-properties-iot-topicruledestination-vpcdestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicruledestination-vpcdestinationproperties-syntax.json"></a>

```
{
  "[RoleArn](#cfn-iot-topicruledestination-vpcdestinationproperties-rolearn)" : String,
  "[SecurityGroups](#cfn-iot-topicruledestination-vpcdestinationproperties-securitygroups)" : [ String, ... ],
  "[SubnetIds](#cfn-iot-topicruledestination-vpcdestinationproperties-subnetids)" : [ String, ... ],
  "[VpcId](#cfn-iot-topicruledestination-vpcdestinationproperties-vpcid)" : String
}
```

### YAML<a name="aws-properties-iot-topicruledestination-vpcdestinationproperties-syntax.yaml"></a>

```
  [RoleArn](#cfn-iot-topicruledestination-vpcdestinationproperties-rolearn): String
  [SecurityGroups](#cfn-iot-topicruledestination-vpcdestinationproperties-securitygroups): 
    - String
  [SubnetIds](#cfn-iot-topicruledestination-vpcdestinationproperties-subnetids): 
    - String
  [VpcId](#cfn-iot-topicruledestination-vpcdestinationproperties-vpcid): String
```

## Properties<a name="aws-properties-iot-topicruledestination-vpcdestinationproperties-properties"></a>

`RoleArn`  <a name="cfn-iot-topicruledestination-vpcdestinationproperties-rolearn"></a>
The ARN of a role that has permission to create and attach to elastic network interfaces \(ENIs\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-iot-topicruledestination-vpcdestinationproperties-securitygroups"></a>
The security groups of the VPC destination\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-iot-topicruledestination-vpcdestinationproperties-subnetids"></a>
The subnet IDs of the VPC destination\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-iot-topicruledestination-vpcdestinationproperties-vpcid"></a>
The ID of the VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)