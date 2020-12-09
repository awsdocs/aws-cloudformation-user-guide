# Setting up VPC endpoints for AWS CloudFormation<a name="cfn-vpce-bucketnames"></a>

You can improve the security posture of your VPC by configuring AWS CloudFormation to use an interface VPC endpoint\. Interface endpoints are powered by PrivateLink, a technology that enables you to privately access AWS CloudFormation APIs by using private IP addresses\. PrivateLink restricts all network traffic between your VPC and AWS CloudFormation to the Amazon network\. Also, you don't need an Internet gateway, a NAT device, or a virtual private gateway\. 

You are not required to configure PrivateLink, but it's recommended\. For more information about PrivateLink and VPC endpoints, see [Accessing AWS services through PrivateLink](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Introduction.html#what-is-privatelink)\.

## Before you begin<a name="cfn-setting-up-vpc-considerations"></a>

Before you configure VPC endpoints for AWS CloudFormation, be aware of the following considerations\.
+ When using the VPC endpoint feature, grant access to AWS CloudFormation\-specific S3 buckets for resources in a VPC that must respond to a custom resource request or a wait condition\.

   If you use AWS CloudFormation to create resources in a VPC with a VPC endpoint, you might need to modify your IAM endpoint policy so that it permits access to certain S3 buckets\.

  AWS CloudFormation has S3 buckets in each Region to monitor responses to a [custom resource](template-custom-resources.md) request or a [wait condition](using-cfn-waitcondition.md)\. If a template includes custom resources or wait conditions in a VPC, the VPC endpoint policy must allow users to send responses to the following buckets:
  + For custom resources, permit traffic to the `cloudformation-custom-resource-response-region` bucket\. When using custom resources, region names do not contain dashes\. For example, `uswest2`\.
  + For wait conditions, permit traffic to the `cloudformation-waitcondition-region` bucket\. When using wait conditions, region names do contain dashes\. For example, `us-west-2`\.

  If the endpoint policy blocks traffic to these buckets, AWS CloudFormation won't receive responses and the stack operation fails\. For example, if you have a resource in a VPC in the `us-west-2` Region that must respond to a wait condition, the resource must be able to send a response to the `cloudformation-waitcondition-us-west-2` bucket\.

  For a list of Regions that AWS CloudFormation supports, see the [Regions and endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region) page in the *Amazon Web Services General Reference*\.
+ VPC endpoints currently do not support cross\-Region requests—ensure that you create your endpoint in the same Region in which you plan to issue your API calls to AWS CloudFormation\. 
+ VPC endpoints only support Amazon\-provided DNS through Route 53\. If you want to use your own DNS, you can use conditional DNS forwarding\. For more information, see [DHCP options sets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html) in the Amazon VPC User Guide\.
+ The security group attached to the VPC endpoint must allow incoming connections on port 443 from the private subnet of the VPC\.

## Creating the VPC EndPoint for AWS CloudFormation<a name="cfn-setting-up-vpc-create"></a>

To create the VPC endpoint for the AWS CloudFormation service, use the [Creating an interface endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpce-interface.html#create-interface-endpoint) procedure in the Amazon VPC User Guide to create the following endpoint:

**com\.amazonaws\.*region*\.cloudformation**

*region* represents the region identifier for an AWS region supported by AWS CloudFormation, such as `us-east-2` for the US East \(Ohio\) Region\. 