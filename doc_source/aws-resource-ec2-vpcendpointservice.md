# AWS::EC2::VPCEndpointService<a name="aws-resource-ec2-vpcendpointservice"></a>

Specifies a VPC endpoint service configuration to which service consumers \(AWS accounts, IAM users, and IAM roles\) can connect\. Service consumers can create an interface VPC endpoint to connect to your service\.

To create an endpoint service configuration, you must first create a Network Load Balancer for your service\.

## Syntax<a name="aws-resource-ec2-vpcendpointservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointservice-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointService",
  "Properties" : {
      "[AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired)" : Boolean,
      "[NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointservice-syntax.yaml"></a>

```
Type: AWS::EC2::VPCEndpointService
Properties: 
  [AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired): Boolean
  [NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns): 
    - String
```

## Properties<a name="aws-resource-ec2-vpcendpointservice-properties"></a>

`AcceptanceRequired`  <a name="cfn-ec2-vpcendpointservice-acceptancerequired"></a>
Indicates whether requests from service consumers to create an endpoint to your service must be accepted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkLoadBalancerArns`  <a name="cfn-ec2-vpcendpointservice-networkloadbalancerarns"></a>
The Amazon Resource Names \(ARNs\) of one or more Network Load Balancers for your service\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-vpcendpointservice-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcendpointservice-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC endpoint service configuration\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-ec2-vpcendpointservice--seealso"></a>
+ [CreateVpcEndpointServiceConfiguration](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpcEndpointServiceConfiguration.html) in the *Amazon EC2 API Reference*
+ [VPC Endpoint Services](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/endpoint-service.html) in the *Amazon Virtual Private Cloud User Guide*