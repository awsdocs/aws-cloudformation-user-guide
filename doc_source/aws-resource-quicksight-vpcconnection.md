# AWS::QuickSight::VPCConnection<a name="aws-resource-quicksight-vpcconnection"></a>

<a name="aws-resource-quicksight-vpcconnection-description"></a>The `AWS::QuickSight::VPCConnection` resource Property description not available\. for QuickSight\.

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
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AwsAccountId`  <a name="cfn-quicksight-vpcconnection-awsaccountid"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DnsResolvers`  <a name="cfn-quicksight-vpcconnection-dnsresolvers"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-vpcconnection-name"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-quicksight-vpcconnection-rolearn"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-quicksight-vpcconnection-securitygroupids"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-quicksight-vpcconnection-subnetids"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-vpcconnection-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCConnectionId`  <a name="cfn-quicksight-vpcconnection-vpcconnectionid"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-quicksight-vpcconnection-return-values"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-vpcconnection-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-vpcconnection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Property description not available\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Property description not available\.

`NetworkInterfaces`  <a name="NetworkInterfaces-fn::getatt"></a>
Property description not available\.

`Status`  <a name="Status-fn::getatt"></a>
Property description not available\.

`VPCId`  <a name="VPCId-fn::getatt"></a>
Property description not available\.