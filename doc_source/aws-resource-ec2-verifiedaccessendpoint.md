# AWS::EC2::VerifiedAccessEndpoint<a name="aws-resource-ec2-verifiedaccessendpoint"></a>

An AWS Verified Access endpoint specifies the application that AWS Verified Access provides access to\. It must be attached to an AWS Verified Access group\. An AWS Verified Access endpoint must also have an attached access policy before you attached it to a group\.

## Syntax<a name="aws-resource-ec2-verifiedaccessendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-verifiedaccessendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VerifiedAccessEndpoint",
  "Properties" : {
      "[ApplicationDomain](#cfn-ec2-verifiedaccessendpoint-applicationdomain)" : String,
      "[AttachmentType](#cfn-ec2-verifiedaccessendpoint-attachmenttype)" : String,
      "[Description](#cfn-ec2-verifiedaccessendpoint-description)" : String,
      "[DomainCertificateArn](#cfn-ec2-verifiedaccessendpoint-domaincertificatearn)" : String,
      "[EndpointDomainPrefix](#cfn-ec2-verifiedaccessendpoint-endpointdomainprefix)" : String,
      "[EndpointType](#cfn-ec2-verifiedaccessendpoint-endpointtype)" : String,
      "[LoadBalancerOptions](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions)" : LoadBalancerOptions,
      "[NetworkInterfaceOptions](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions)" : NetworkInterfaceOptions,
      "[PolicyDocument](#cfn-ec2-verifiedaccessendpoint-policydocument)" : String,
      "[PolicyEnabled](#cfn-ec2-verifiedaccessendpoint-policyenabled)" : Boolean,
      "[SecurityGroupIds](#cfn-ec2-verifiedaccessendpoint-securitygroupids)" : [ String, ... ],
      "[Tags](#cfn-ec2-verifiedaccessendpoint-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VerifiedAccessGroupId](#cfn-ec2-verifiedaccessendpoint-verifiedaccessgroupid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-verifiedaccessendpoint-syntax.yaml"></a>

```
Type: AWS::EC2::VerifiedAccessEndpoint
Properties: 
  [ApplicationDomain](#cfn-ec2-verifiedaccessendpoint-applicationdomain): String
  [AttachmentType](#cfn-ec2-verifiedaccessendpoint-attachmenttype): String
  [Description](#cfn-ec2-verifiedaccessendpoint-description): String
  [DomainCertificateArn](#cfn-ec2-verifiedaccessendpoint-domaincertificatearn): String
  [EndpointDomainPrefix](#cfn-ec2-verifiedaccessendpoint-endpointdomainprefix): String
  [EndpointType](#cfn-ec2-verifiedaccessendpoint-endpointtype): String
  [LoadBalancerOptions](#cfn-ec2-verifiedaccessendpoint-loadbalanceroptions): 
    LoadBalancerOptions
  [NetworkInterfaceOptions](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions): 
    NetworkInterfaceOptions
  [PolicyDocument](#cfn-ec2-verifiedaccessendpoint-policydocument): String
  [PolicyEnabled](#cfn-ec2-verifiedaccessendpoint-policyenabled): Boolean
  [SecurityGroupIds](#cfn-ec2-verifiedaccessendpoint-securitygroupids): 
    - String
  [Tags](#cfn-ec2-verifiedaccessendpoint-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VerifiedAccessGroupId](#cfn-ec2-verifiedaccessendpoint-verifiedaccessgroupid): String
```

## Properties<a name="aws-resource-ec2-verifiedaccessendpoint-properties"></a>

`ApplicationDomain`  <a name="cfn-ec2-verifiedaccessendpoint-applicationdomain"></a>
The DNS name for users to reach your application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AttachmentType`  <a name="cfn-ec2-verifiedaccessendpoint-attachmenttype"></a>
The type of attachment used to provide connectivity between the AWS Verified Access endpoint and the application\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `vpc`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-verifiedaccessendpoint-description"></a>
A description for the AWS Verified Access endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainCertificateArn`  <a name="cfn-ec2-verifiedaccessendpoint-domaincertificatearn"></a>
The ARN of a public TLS/SSL certificate imported into or created with ACM\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointDomainPrefix`  <a name="cfn-ec2-verifiedaccessendpoint-endpointdomainprefix"></a>
A custom identifier that is prepended to the DNS name that is generated for the endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointType`  <a name="cfn-ec2-verifiedaccessendpoint-endpointtype"></a>
The type of AWS Verified Access endpoint\. Incoming application requests will be sent to an IP address, load balancer or a network interface depending on the endpoint type specified\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `load-balancer | network-interface`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoadBalancerOptions`  <a name="cfn-ec2-verifiedaccessendpoint-loadbalanceroptions"></a>
The load balancer details if creating the AWS Verified Access endpoint as `load-balancer`type\.  
*Required*: No  
*Type*: [LoadBalancerOptions](aws-properties-ec2-verifiedaccessendpoint-loadbalanceroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceOptions`  <a name="cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions"></a>
The options for network\-interface type endpoint\.  
*Required*: No  
*Type*: [NetworkInterfaceOptions](aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDocument`  <a name="cfn-ec2-verifiedaccessendpoint-policydocument"></a>
The Verified Access policy document\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyEnabled`  <a name="cfn-ec2-verifiedaccessendpoint-policyenabled"></a>
The status of the Verified Access policy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-ec2-verifiedaccessendpoint-securitygroupids"></a>
The IDs of the security groups for the endpoint\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-verifiedaccessendpoint-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifiedAccessGroupId`  <a name="cfn-ec2-verifiedaccessendpoint-verifiedaccessgroupid"></a>
The ID of the AWS Verified Access group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-verifiedaccessendpoint-return-values"></a>

### Ref<a name="aws-resource-ec2-verifiedaccessendpoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Verified Access endpoint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-verifiedaccessendpoint-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-verifiedaccessendpoint-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The creation time\.

`DeletionTime`  <a name="DeletionTime-fn::getatt"></a>
Property description not available\.

`DeviceValidationDomain`  <a name="DeviceValidationDomain-fn::getatt"></a>
Use this to construct the redirect URI to add to your OIDC provider's allow list\.

`EndpointDomain`  <a name="EndpointDomain-fn::getatt"></a>
The DNS name generated for the endpoint\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The last updated time\.

`Status`  <a name="Status-fn::getatt"></a>
The endpoint status\.

`Status.Code`  <a name="Status.Code-fn::getatt"></a>
Property description not available\.

`Status.Message`  <a name="Status.Message-fn::getatt"></a>
Property description not available\.

`VerifiedAccessEndpointId`  <a name="VerifiedAccessEndpointId-fn::getatt"></a>
The ID of the Verified Access endpoint\.

`VerifiedAccessInstanceId`  <a name="VerifiedAccessInstanceId-fn::getatt"></a>
The instance identifier\.