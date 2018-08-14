# AWS CloudFormation and VPC Endpoints<a name="cfn-vpce-bucketnames"></a>

You can use a [VPC endpoint](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-endpoints.html) to create a private connection between your VPC and another AWS service without requiring access over the Internet, through a NAT instance, a VPN connection, or AWS Direct Connect\. If you use AWS CloudFormation to create resources in a VPC with a VPC endpoint, you might need to modify your IAM endpoint policy so that it permits access to certain S3 buckets\.

AWS CloudFormation has S3 buckets in each region to monitor responses to a [custom resource](template-custom-resources.md) request or a [wait condition](using-cfn-waitcondition.md)\. If a template includes custom resources or wait conditions in a VPC, the VPC endpoint policy must allow users to send responses to the following buckets:
+ For custom resources, permit traffic to the `cloudformation-custom-resource-response-region` bucket\.
+ For wait conditions, permit traffic to the `cloudformation-waitcondition-region` bucket\.

If the endpoint policy blocks traffic to these buckets, AWS CloudFormation won't receive responses and the stack operation fails\. For example, if you have a resource in a VPC in the `us-west-2` region that must respond to a wait condition, the resource must be able to send a response to the `cloudformation-waitcondition-us-west-2` bucket\.

For a list of regions that AWS CloudFormation supports, see the [Regions and Endpoints](http://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region) page in the *Amazon Web Services General Reference*\.