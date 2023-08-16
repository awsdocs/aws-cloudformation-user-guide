# AWS::MSK::VpcConnection<a name="aws-resource-msk-vpcconnection"></a>

Create remote VPC connection\.

## Syntax<a name="aws-resource-msk-vpcconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-vpcconnection-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::VpcConnection",
  "Properties" : {
      "[Authentication](#cfn-msk-vpcconnection-authentication)" : String,
      "[ClientSubnets](#cfn-msk-vpcconnection-clientsubnets)" : [ String, ... ],
      "[SecurityGroups](#cfn-msk-vpcconnection-securitygroups)" : [ String, ... ],
      "[Tags](#cfn-msk-vpcconnection-tags)" : {Key: Value, ...},
      "[TargetClusterArn](#cfn-msk-vpcconnection-targetclusterarn)" : String,
      "[VpcId](#cfn-msk-vpcconnection-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-msk-vpcconnection-syntax.yaml"></a>

```
Type: AWS::MSK::VpcConnection
Properties: 
  [Authentication](#cfn-msk-vpcconnection-authentication): String
  [ClientSubnets](#cfn-msk-vpcconnection-clientsubnets): 
    - String
  [SecurityGroups](#cfn-msk-vpcconnection-securitygroups): 
    - String
  [Tags](#cfn-msk-vpcconnection-tags): 
    Key: Value
  [TargetClusterArn](#cfn-msk-vpcconnection-targetclusterarn): String
  [VpcId](#cfn-msk-vpcconnection-vpcid): String
```

## Properties<a name="aws-resource-msk-vpcconnection-properties"></a>

`Authentication`  <a name="cfn-msk-vpcconnection-authentication"></a>
The type of private link authentication\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientSubnets`  <a name="cfn-msk-vpcconnection-clientsubnets"></a>
The list of subnets in the client VPC to connect to\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-msk-vpcconnection-securitygroups"></a>
The security groups to attach to the ENIs for the broker nodes\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-msk-vpcconnection-tags"></a>
Create tags when creating the VPC connection\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetClusterArn`  <a name="cfn-msk-vpcconnection-targetclusterarn"></a>
The Amazon Resource Name \(ARN\) of the cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-msk-vpcconnection-vpcid"></a>
The VPC id of the remote client\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-msk-vpcconnection-return-values"></a>

### Ref<a name="aws-resource-msk-vpcconnection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Amazon Resource Name \(ARN\) of the VPC connection\.

For Amazon MSK VPC connection `MyVpcConnection`, `Ref` returns the ARN of the VPC connection whose logical ID is `MyVpcConnection`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-msk-vpcconnection-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-msk-vpcconnection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the VPC connection\.