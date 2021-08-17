# AWS::SageMaker::Domain<a name="aws-resource-sagemaker-domain"></a>

Creates a `Domain` used by Amazon SageMaker Studio\. A domain consists of an associated Amazon Elastic File System \(EFS\) volume, a list of authorized users, and a variety of security, application, policy, and Amazon Virtual Private Cloud \(VPC\) configurations\. An AWS account is limited to one domain per region\. Users within a domain can share notebook files and other artifacts with each other\.

 **EFS storage** 

When a domain is created, an EFS volume is created for use by all of the users within the domain\. Each user receives a private home directory within the EFS volume for notebooks, Git repositories, and data files\.

SageMaker uses the AWS Key Management Service \(AWS KMS\) to encrypt the EFS volume attached to the domain with an AWS managed customer master key \(CMK\) by default\. For more control, you can specify a customer managed CMK\. For more information, see [Protect Data at Rest Using Encryption](https://docs.aws.amazon.com/sagemaker/latest/dg/encryption-at-rest.html)\.

 **VPC configuration** 

All SageMaker Studio traffic between the domain and the EFS volume is through the specified VPC and subnets\. For other Studio traffic, you can specify the `AppNetworkAccessType` parameter\. `AppNetworkAccessType` corresponds to the network access type that you choose when you onboard to Studio\. The following options are available:
+  `PublicInternetOnly` \- Non\-EFS traffic goes through a VPC managed by Amazon SageMaker, which allows internet access\. This is the default value\.
+  `VpcOnly` \- All Studio traffic is through the specified VPC and subnets\. Internet access is disabled by default\. To allow internet access, you must specify a NAT gateway\.

  When internet access is disabled, you won't be able to run a Studio notebook or to train or host models unless your VPC has an interface endpoint to the SageMaker API and runtime or a NAT gateway and your security groups allow outbound connections\.

**Important**  
NFS traffic over TCP on port 2049 needs to be allowed in both inbound and outbound rules in order to launch a SageMaker Studio app successfully\.

For more information, see [Connect SageMaker Studio Notebooks to Resources in a VPC](https://docs.aws.amazon.com/sagemaker/latest/dg/studio-notebooks-and-internet-access.html)\.

## Syntax<a name="aws-resource-sagemaker-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-domain-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Domain",
  "Properties" : {
      "[AppNetworkAccessType](#cfn-sagemaker-domain-appnetworkaccesstype)" : String,
      "[AuthMode](#cfn-sagemaker-domain-authmode)" : String,
      "[DefaultUserSettings](#cfn-sagemaker-domain-defaultusersettings)" : UserSettings,
      "[DomainName](#cfn-sagemaker-domain-domainname)" : String,
      "[KmsKeyId](#cfn-sagemaker-domain-kmskeyid)" : String,
      "[SubnetIds](#cfn-sagemaker-domain-subnetids)" : [ String, ... ],
      "[Tags](#cfn-sagemaker-domain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-sagemaker-domain-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-sagemaker-domain-syntax.yaml"></a>

```
Type: AWS::SageMaker::Domain
Properties: 
  [AppNetworkAccessType](#cfn-sagemaker-domain-appnetworkaccesstype): String
  [AuthMode](#cfn-sagemaker-domain-authmode): String
  [DefaultUserSettings](#cfn-sagemaker-domain-defaultusersettings): 
    UserSettings
  [DomainName](#cfn-sagemaker-domain-domainname): String
  [KmsKeyId](#cfn-sagemaker-domain-kmskeyid): String
  [SubnetIds](#cfn-sagemaker-domain-subnetids): 
    - String
  [Tags](#cfn-sagemaker-domain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-sagemaker-domain-vpcid): String
```

## Properties<a name="aws-resource-sagemaker-domain-properties"></a>

`AppNetworkAccessType`  <a name="cfn-sagemaker-domain-appnetworkaccesstype"></a>
Specifies the VPC used for non\-EFS traffic\. The default value is `PublicInternetOnly`\.  
+ `PublicInternetOnly` \- Non\-EFS traffic is through a VPC managed by Amazon SageMaker, which allows direct internet access
+ `VpcOnly` \- All Studio traffic is through the specified VPC and subnets
*Valid Values*: `PublicInternetOnly | VpcOnly`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthMode`  <a name="cfn-sagemaker-domain-authmode"></a>
The mode of authentication that members use to access the domain\.  
*Valid Values*: `SSO | IAM`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultUserSettings`  <a name="cfn-sagemaker-domain-defaultusersettings"></a>
The default user settings\.  
*Required*: Yes  
*Type*: [UserSettings](aws-properties-sagemaker-domain-usersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-sagemaker-domain-domainname"></a>
The domain name\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-sagemaker-domain-kmskeyid"></a>
SageMaker uses AWS KMS to encrypt the EFS volume attached to the domain with an AWS managed customer master key \(CMK\) by default\. For more control, specify a customer managed CMK\.  
*Length Constraints*: Maximum length of 2048\.  
*Pattern*: `.*`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-sagemaker-domain-subnetids"></a>
The VPC subnets that Studio uses for communication\.  
*Length Constraints*: Maximum length of 32\.  
*Array members*: Minimum number of 1 item\. Maximum number of 16 items\.  
*Pattern*: `[-0-9a-zA-Z]+`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-sagemaker-domain-tags"></a>
Tags to associated with the Domain\. Each tag consists of a key and an optional value\. Tag keys must be unique per resource\. Tags are searchable using the Search API\.   
Tags that you specify for the Domain are also added to all Apps that are launched in the Domain\.  
*Array members*: Minimum number of 0 items\. Maximum number of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-sagemaker-domain-vpcid"></a>
The ID of the Amazon Virtual Private Cloud \(VPC\) that Studio uses for communication\.  
*Length Constraints*: Maximum length of 32\.  
*Pattern*: `[-0-9a-zA-Z]+`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-domain-return-values"></a>

### Ref<a name="aws-resource-sagemaker-domain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the domain ID, such as `d-xxxxxxxxxxxx`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-domain-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sagemaker-domain-return-values-fn--getatt-fn--getatt"></a>

`DomainArn`  <a name="DomainArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the domain, such as `arn:aws:sagemaker:us-west-2:account-id:domain/my-domain-name`\.

`DomainId`  <a name="DomainId-fn::getatt"></a>
The domain ID\.

`HomeEfsFileSystemId`  <a name="HomeEfsFileSystemId-fn::getatt"></a>
The ID of the Amazon Elastic File System \(EFS\) managed by this Domain\.

`SingleSignOnManagedApplicationInstanceId`  <a name="SingleSignOnManagedApplicationInstanceId-fn::getatt"></a>
The AWS SSO managed application instance ID\.

`Url`  <a name="Url-fn::getatt"></a>
The URL for the domain\.