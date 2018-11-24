# AWS::EC2::VPCEndpointService<a name="aws-resource-ec2-vpcendpointservice"></a>

Creates a VPC endpoint service configuration to which service consumers \(AWS accounts, IAM users, and IAM roles\) can connect\. Service consumers can create an interface VPC endpoint to connect to your service\. For more information, see [CreateVpcEndpointServiceConfiguration](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcEndpointServiceConfiguration.html)\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcendpointservice-syntax)
+ [Properties](#aws-resource-ec2-vpcendpointservice-properties)
+ [Return Values](#aws-resource-ec2-vpcendpointservice-returnvalues)

## Syntax<a name="aws-resource-ec2-vpcendpointservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointservice-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointService",
  "Properties" : {
    "[NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns)" : [ String, ... ],
    "[AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired)" : Boolean
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointservice-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCEndpointService"
Properties:
  [NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns): 
    - String
  [AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired): Boolean
```

## Properties<a name="aws-resource-ec2-vpcendpointservice-properties"></a>

`AcceptanceRequired`  <a name="cfn-ec2-vpcendpointservice-acceptancerequired"></a>
Indicate whether requests from service consumers to create an endpoint to your service must be accepted\. To accept a request, use [AcceptVpcEndpointConnections](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AcceptVpcEndpointConnections.html)\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NetworkLoadBalancerArns`  <a name="cfn-ec2-vpcendpointservice-networkloadbalancerarns"></a>
The Amazon Resource Names \(ARNs\) of one or more Network Load Balancers for your service\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ec2-vpcendpointservice-returnvalues"></a>

### Ref<a name="aws-resource-ec2-vpcendpointservice-ref"></a>

When you pass the logical ID of an `AWS::EC2::VPCEndpointService` resource to the intrinsic `Ref` function, the function returns the ID of the VPC endpoint service configuration\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.