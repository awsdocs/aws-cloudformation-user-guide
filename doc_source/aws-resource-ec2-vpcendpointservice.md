# AWS::EC2::VPCEndpointService<a name="aws-resource-ec2-vpcendpointservice"></a>

Creates a VPC endpoint service configuration to which service consumers \(AWS accounts, users, and IAM roles\) can connect\.

To create an endpoint service configuration, you must first create one of the following for your service:
+ A [Network Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html)\. Service consumers connect to your service using an interface endpoint\.
+ A [Gateway Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/introduction.html)\. Service consumers connect to your service using a Gateway Load Balancer endpoint\.

For more information, see the [AWS PrivateLink User Guide](https://docs.aws.amazon.com/vpc/latest/privatelink/)\.

## Syntax<a name="aws-resource-ec2-vpcendpointservice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointservice-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointService",
  "Properties" : {
      "[AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired)" : Boolean,
      "[ContributorInsightsEnabled](#cfn-ec2-vpcendpointservice-contributorinsightsenabled)" : Boolean,
      "[GatewayLoadBalancerArns](#cfn-ec2-vpcendpointservice-gatewayloadbalancerarns)" : [ String, ... ],
      "[NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns)" : [ String, ... ],
      "[PayerResponsibility](#cfn-ec2-vpcendpointservice-payerresponsibility)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointservice-syntax.yaml"></a>

```
Type: AWS::EC2::VPCEndpointService
Properties: 
  [AcceptanceRequired](#cfn-ec2-vpcendpointservice-acceptancerequired): Boolean
  [ContributorInsightsEnabled](#cfn-ec2-vpcendpointservice-contributorinsightsenabled): Boolean
  [GatewayLoadBalancerArns](#cfn-ec2-vpcendpointservice-gatewayloadbalancerarns): 
    - String
  [NetworkLoadBalancerArns](#cfn-ec2-vpcendpointservice-networkloadbalancerarns): 
    - String
  [PayerResponsibility](#cfn-ec2-vpcendpointservice-payerresponsibility): String
```

## Properties<a name="aws-resource-ec2-vpcendpointservice-properties"></a>

`AcceptanceRequired`  <a name="cfn-ec2-vpcendpointservice-acceptancerequired"></a>
Indicates whether requests from service consumers to create an endpoint to your service must be accepted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContributorInsightsEnabled`  <a name="cfn-ec2-vpcendpointservice-contributorinsightsenabled"></a>
Indicates whether to enable the built\-in Contributor Insights rules\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GatewayLoadBalancerArns`  <a name="cfn-ec2-vpcendpointservice-gatewayloadbalancerarns"></a>
The Amazon Resource Names \(ARNs\) of the Gateway Load Balancers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkLoadBalancerArns`  <a name="cfn-ec2-vpcendpointservice-networkloadbalancerarns"></a>
The Amazon Resource Names \(ARNs\) of the Network Load Balancers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayerResponsibility`  <a name="cfn-ec2-vpcendpointservice-payerresponsibility"></a>
The entity that is responsible for the endpoint costs\. The default is the endpoint owner\. If you set the payer responsibility to the service owner, you cannot set it back to the endpoint owner\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ServiceOwner`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-vpcendpointservice-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcendpointservice-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC endpoint service configuration\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-vpcendpointservice-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-vpcendpointservice-return-values-fn--getatt-fn--getatt"></a>

`ServiceId`  <a name="ServiceId-fn::getatt"></a>
Property description not available\.

## See also<a name="aws-resource-ec2-vpcendpointservice--seealso"></a>
+ [CreateVpcEndpointServiceConfiguration](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpcEndpointServiceConfiguration.html) in the *Amazon EC2 API Reference*
+ [VPC endpoint services](https://docs.aws.amazon.com/vpc/latest/privatelink/endpoint-service.html) in *AWS PrivateLink*

