# AWS CloudFormation and interface VPC endpoints \(AWS PrivateLink\)<a name="vpc-interface-endpoints"></a>

You can establish a private connection between your VPC and AWS CloudFormation by creating an *interface VPC endpoint*\. Interface endpoints are powered by [AWS PrivateLink](http://aws.amazon.com/privatelink), a technology that enables you to privately access CloudFormation APIs without an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection\. Instances in your VPC don't need public IP addresses to communicate with CloudFormation APIs\. Traffic between your VPC and CloudFormation doesn't keep the Amazon network\.

Each interface endpoint is represented by one or more [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html) in your subnets\.

For more information, see [Interface VPC endpoints \(AWS PrivateLink\)](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html) in the *Amazon VPC User Guide*\.

## Considerations for CloudFormation VPC endpoints<a name="vpc-endpoint-considerations"></a>

Before you set up an interface VPC endpoint for CloudFormation, ensure that you review [Interface endpoint properties and limitations](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html#vpce-interface-limitations) in the *Amazon VPC User Guide*\.

CloudFormation supports making calls to all of its API actions from your VPC\.

## Creating an interface VPC endpoint for CloudFormation<a name="vpc-endpoint-create"></a>

You can create a VPC endpoint for the CloudFormation service using either the Amazon VPC console or the AWS Command Line Interface \(AWS CLI\)\. For more information, see [Creating an interface endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html#create-interface-endpoint) in the *Amazon VPC User Guide*\.

Create a VPC endpoint for CloudFormation using the following service name: 
+ com\.amazonaws\.*region*\.cloudformation

If you enable private DNS for the endpoint, you can make API requests to CloudFormation using its default DNS name for the Region, for example, `cloudformation.us-east-1.amazonaws.com`\.

For more information, see [Accessing a service through an interface endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html#access-service-though-endpoint) in the *Amazon VPC User Guide*\.

## Creating a VPC endpoint policy for CloudFormation<a name="vpc-endpoint-policy"></a>

You can attach an endpoint policy to your VPC endpoint that controls access to CloudFormation\. The policy specifies the following information:
+ The principal that can perform actions\.
+ The actions that can be performed\.
+ The resources on which actions can be performed\.

For more information, see [Controlling access to services with VPC endpoints](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints-access.html) in the *Amazon VPC User Guide*\.

**Example: VPC endpoint policy for CloudFormation actions**  
The following is an example of an endpoint policy for CloudFormation\. When attached to an endpoint, this policy grants access to the listed CloudFormation actions for all principals on all resources\. The following example denies all users the permission to create stacks through the VPC endpoint, and allows full access to all other actions on the CloudFormation service\.

```
{
  "Statement": [
    {
      "Action": "cloudformation:*", 
      "Effect": "Allow", 
      "Principal": "*", 
      "Resource": "*"
    },
    {
      "Action": "cloudformation:CreateStack", 
      "Effect": "Deny", 
      "Principal": "*", 
      "Resource": "*"
    }
  ]
}
```

## See also<a name="see-also"></a>
+ [AWS services that integrate with AWS PrivateLink](https://docs.aws.amazon.com/vpc/latest/privatelink/integrated-services-vpce-list.html)
+ [Setting up VPC endpoints for AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-vpce-bucketnames.html)