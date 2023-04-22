# AWS::EC2::VerifiedAccessInstance VerifiedAccessTrustProvider<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider"></a>

Describes a Verified Access trust provider\.

## Syntax<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-syntax.json"></a>

```
{
  "[Description](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-description)" : String,
  "[DeviceTrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-devicetrustprovidertype)" : String,
  "[TrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-trustprovidertype)" : String,
  "[UserTrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-usertrustprovidertype)" : String,
  "[VerifiedAccessTrustProviderId](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-verifiedaccesstrustproviderid)" : String
}
```

### YAML<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-syntax.yaml"></a>

```
  [Description](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-description): String
  [DeviceTrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-devicetrustprovidertype): String
  [TrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-trustprovidertype): String
  [UserTrustProviderType](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-usertrustprovidertype): String
  [VerifiedAccessTrustProviderId](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-verifiedaccesstrustproviderid): String
```

## Properties<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-properties"></a>

`Description`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-description"></a>
A description for the AWS Verified Access trust provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceTrustProviderType`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-devicetrustprovidertype"></a>
The type of device\-based trust provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `crowdstrike | jamf`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustProviderType`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-trustprovidertype"></a>
The type of Verified Access trust provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `device | user`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserTrustProviderType`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-usertrustprovidertype"></a>
The type of user\-based trust provider\.  
*Required*: No  
*Type*: String  
*Allowed values*: `iam-identity-center | oidc`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifiedAccessTrustProviderId`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustprovider-verifiedaccesstrustproviderid"></a>
The ID of the AWS Verified Access trust provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)