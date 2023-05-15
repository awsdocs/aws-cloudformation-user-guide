# AWS::EC2::VerifiedAccessEndpoint LoadBalancerOptions<a name="aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions"></a>

Describes the load balancer options when creating an AWS Verified Access endpoint using the `load-balancer` type\.

## Syntax<a name="aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions-syntax.json"></a>

```
{
  "[LoadBalancerArn](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-loadbalancerarn)" : String,
  "[Port](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-port)" : Integer,
  "[Protocol](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-protocol)" : String,
  "[SubnetIds](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions-syntax.yaml"></a>

```
  [LoadBalancerArn](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-loadbalancerarn): String
  [Port](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-port): Integer
  [Protocol](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-protocol): String
  [SubnetIds](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-subnetids): 
    - String
```

## Properties<a name="aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions-properties"></a>

`LoadBalancerArn`  <a name="cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-loadbalancerarn"></a>
The ARN of the load balancer\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-port"></a>
The IP port number\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-protocol"></a>
The IP protocol\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-ec2-verifiedaccessendpoint-loadbalanceroptions-subnetids"></a>
The IDs of the subnets\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)