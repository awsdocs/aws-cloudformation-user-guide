# AWS::QuickSight::VPCConnection<a name="aws-resource-quicksight-vpcconnection"></a>

Creates a new VPC connection\.

## Syntax<a name="aws-resource-quicksight-vpcconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-vpcconnection-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::VPCConnection",
  "Properties" : {
      "[AvailabilityStatus](#cfn-quicksight-vpcconnection-availabilitystatus)" : String,
      "[AwsAccountId](#cfn-quicksight-vpcconnection-awsaccountid)" : String,
      "[DnsResolvers](#cfn-quicksight-vpcconnection-dnsresolvers)" : [ String, ... ],
      "[Name](#cfn-quicksight-vpcconnection-name)" : String,
      "[RoleArn](#cfn-quicksight-vpcconnection-rolearn)" : String,
      "[SecurityGroupIds](#cfn-quicksight-vpcconnection-securitygroupids)" : [ String, ... ],
      "[SubnetIds](#cfn-quicksight-vpcconnection-subnetids)" : [ String, ... ],
      "[Tags](#cfn-quicksight-vpcconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VPCConnectionId](#cfn-quicksight-vpcconnection-vpcconnectionid)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-vpcconnection-syntax.yaml"></a>

```
Type: AWS::QuickSight::VPCConnection
Properties: 
  [AvailabilityStatus](#cfn-quicksight-vpcconnection-availabilitystatus): String
  [AwsAccountId](#cfn-quicksight-vpcconnection-awsaccountid): String
  [DnsResolvers](#cfn-quicksight-vpcconnection-dnsresolvers): 
    - String
  [Name](#cfn-quicksight-vpcconnection-name): String
  [RoleArn](#cfn-quicksight-vpcconnection-rolearn): String
  [SecurityGroupIds](#cfn-quicksight-vpcconnection-securitygroupids): 
    - String
  [SubnetIds](#cfn-quicksight-vpcconnection-subnetids): 
    - String
  [Tags](#cfn-quicksight-vpcconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VPCConnectionId](#cfn-quicksight-vpcconnection-vpcconnectionid): String
```

## Properties<a name="aws-resource-quicksight-vpcconnection-properties"></a>

`AvailabilityStatus`  <a name="cfn-quicksight-vpcconnection-availabilitystatus"></a>
The availability status of the VPC connection\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AVAILABLE | PARTIALLY_AVAILABLE | UNAVAILABLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsAccountId`  <a name="cfn-quicksight-vpcconnection-awsaccountid"></a>
The AWS account ID of the account where you want to create a new VPC connection\.  
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^[0-9]{12}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DnsResolvers`  <a name="cfn-quicksight-vpcconnection-dnsresolvers"></a>
A list of IP addresses of DNS resolver endpoints for the VPC connection\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-vpcconnection-name"></a>
The display name for the VPC connection\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-quicksight-vpcconnection-rolearn"></a>
The ARN of the IAM role associated with the VPC connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-quicksight-vpcconnection-securitygroupids"></a>
The Amazon EC2 security group IDs associated with the VPC connection\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-quicksight-vpcconnection-subnetids"></a>
A list of subnet IDs for the VPC connection\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-vpcconnection-tags"></a>
A map of the key\-value pairs for the resource tag or tags assigned to the VPC connection\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCConnectionId`  <a name="cfn-quicksight-vpcconnection-vpcconnectionid"></a>
The ID of the VPC connection that you're creating\. This ID is a unique identifier for each AWS Region in an AWS account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-quicksight-vpcconnection-return-values"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-vpcconnection-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-vpcconnection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the VPC connection\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time that the VPC connection was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The time that the VPC connection was last updated\.

`NetworkInterfaces`  <a name="NetworkInterfaces-fn::getatt"></a>
A list of network interfaces\.

`Status`  <a name="Status-fn::getatt"></a>
The HTTP status of the request\.

`VPCId`  <a name="VPCId-fn::getatt"></a>
The ID of the VPC connection that you're creating\. This ID is a unique identifier for each AWS Region in an AWS account\.