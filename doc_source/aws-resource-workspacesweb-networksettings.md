# AWS::WorkSpacesWeb::NetworkSettings<a name="aws-resource-workspacesweb-networksettings"></a>

This resource specifies network settings that can be associated with a web portal\. Once associated with a web portal, network settings define how streaming instances will connect with your specified VPC\.

The VPC must have default tenancy\. VPCs with dedicated tenancy are not supported\.

For availability consideration, you must have at least two subnets created in two different Availability Zones\. WorkSpaces Web is available in a subset of the Availability Zones for each supported Region\. For more information, see [Supported Availability Zones](https://docs.aws.amazon.com/workspaces-web/latest/adminguide/availability-zones.html)\.

## Syntax<a name="aws-resource-workspacesweb-networksettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspacesweb-networksettings-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpacesWeb::NetworkSettings",
  "Properties" : {
      "[SecurityGroupIds](#cfn-workspacesweb-networksettings-securitygroupids)" : [ String, ... ],
      "[SubnetIds](#cfn-workspacesweb-networksettings-subnetids)" : [ String, ... ],
      "[Tags](#cfn-workspacesweb-networksettings-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-workspacesweb-networksettings-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-workspacesweb-networksettings-syntax.yaml"></a>

```
Type: AWS::WorkSpacesWeb::NetworkSettings
Properties: 
  [SecurityGroupIds](#cfn-workspacesweb-networksettings-securitygroupids): 
    - String
  [SubnetIds](#cfn-workspacesweb-networksettings-subnetids): 
    - String
  [Tags](#cfn-workspacesweb-networksettings-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-workspacesweb-networksettings-vpcid): String
```

## Properties<a name="aws-resource-workspacesweb-networksettings-properties"></a>

`SecurityGroupIds`  <a name="cfn-workspacesweb-networksettings-securitygroupids"></a>
One or more security groups used to control access from streaming instances to your VPC\.  
*Pattern*: `^[\w+\-]+$`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-workspacesweb-networksettings-subnetids"></a>
The subnets in which network interfaces are created to connect streaming instances to your VPC\. At least two of these subnets must be in different availability zones\.  
*Pattern*: `^subnet-([0-9a-f]{8}|[0-9a-f]{17})$`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-workspacesweb-networksettings-tags"></a>
The tags to add to the network settings resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-workspacesweb-networksettings-vpcid"></a>
The VPC that streaming instances will connect to\.  
*Pattern*: `^vpc-[0-9a-z]*$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-workspacesweb-networksettings-return-values"></a>

### Ref<a name="aws-resource-workspacesweb-networksettings-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource's Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspacesweb-networksettings-return-values-fn--getatt"></a>

#### <a name="aws-resource-workspacesweb-networksettings-return-values-fn--getatt-fn--getatt"></a>

`AssociatedPortalArns`  <a name="AssociatedPortalArns-fn::getatt"></a>
A list of web portal ARNs that this network settings is associated with\.

`NetworkSettingsArn`  <a name="NetworkSettingsArn-fn::getatt"></a>
The ARN of the network settings\.