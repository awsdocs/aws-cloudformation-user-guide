# AWS::VpcLattice::ServiceNetworkVpcAssociation<a name="aws-resource-vpclattice-servicenetworkvpcassociation"></a>

Associates a VPC with a service network\. When you associate a VPC with the service network, it enables all the resources within that VPC to be clients and communicate with other services in the service network\. For more information, see [Manage VPC associations](https://docs.aws.amazon.com/vpc-lattice/latest/ug/service-network-associations.html#service-network-vpc-associations) in the *Amazon VPC Lattice User Guide*\.

You can't use this operation if there is a disassociation in progress\. If the association fails, retry by deleting the association and recreating it\.

As a result of this operation, the association gets created in the service network account and the VPC owner account\.

If you add a security group to the service network and VPC association, the association must continue to always have at least one security group\. You can add or edit security groups at any time\. However, to remove all security groups, you must first delete the association and recreate it without security groups\.

## Syntax<a name="aws-resource-vpclattice-servicenetworkvpcassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-servicenetworkvpcassociation-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::ServiceNetworkVpcAssociation",
  "Properties" : {
      "[SecurityGroupIds](#cfn-vpclattice-servicenetworkvpcassociation-securitygroupids)" : [ String, ... ],
      "[ServiceNetworkIdentifier](#cfn-vpclattice-servicenetworkvpcassociation-servicenetworkidentifier)" : String,
      "[Tags](#cfn-vpclattice-servicenetworkvpcassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcIdentifier](#cfn-vpclattice-servicenetworkvpcassociation-vpcidentifier)" : String
    }
}
```

### YAML<a name="aws-resource-vpclattice-servicenetworkvpcassociation-syntax.yaml"></a>

```
Type: AWS::VpcLattice::ServiceNetworkVpcAssociation
Properties: 
  [SecurityGroupIds](#cfn-vpclattice-servicenetworkvpcassociation-securitygroupids): 
    - String
  [ServiceNetworkIdentifier](#cfn-vpclattice-servicenetworkvpcassociation-servicenetworkidentifier): String
  [Tags](#cfn-vpclattice-servicenetworkvpcassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcIdentifier](#cfn-vpclattice-servicenetworkvpcassociation-vpcidentifier): String
```

## Properties<a name="aws-resource-vpclattice-servicenetworkvpcassociation-properties"></a>

`SecurityGroupIds`  <a name="cfn-vpclattice-servicenetworkvpcassociation-securitygroupids"></a>
The IDs of the security groups\. Security groups aren't added by default\. You can add a security group to apply network level controls to control which resources in a VPC are allowed to access the service network and its services\. For more information, see [Control traffic to resources using security groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) in the *Amazon VPC User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNetworkIdentifier`  <a name="cfn-vpclattice-servicenetworkvpcassociation-servicenetworkidentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the service network\. You must use the ARN when the resources specified in the operation are in different accounts\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-servicenetworkvpcassociation-tags"></a>
The tags for the association\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcIdentifier`  <a name="cfn-vpclattice-servicenetworkvpcassociation-vpcidentifier"></a>
The ID of the VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-vpclattice-servicenetworkvpcassociation-return-values"></a>

### Ref<a name="aws-resource-vpclattice-servicenetworkvpcassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-servicenetworkvpcassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-servicenetworkvpcassociation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the association between the service network and the VPC\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The date and time that the association was created, specified in ISO\-8601 format\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the specified association between the service network and the VPC\.

`ServiceNetworkArn`  <a name="ServiceNetworkArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service network\.

`ServiceNetworkId`  <a name="ServiceNetworkId-fn::getatt"></a>
The ID of the service network\.

`ServiceNetworkName`  <a name="ServiceNetworkName-fn::getatt"></a>
The name of the service network\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the association\.

`VpcId`  <a name="VpcId-fn::getatt"></a>
The ID of the VPC\.