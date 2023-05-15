# AWS::EC2::VerifiedAccessTrustProvider DeviceOptions<a name="aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions"></a>

Describes the options for an AWS Verified Access device\-identity based trust provider\.

## Syntax<a name="aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions-syntax.json"></a>

```
{
  "[TenantId](#cfn-ec2-verifiedaccesstrustprovider-deviceoptions-tenantid)" : String
}
```

### YAML<a name="aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions-syntax.yaml"></a>

```
  [TenantId](#cfn-ec2-verifiedaccesstrustprovider-deviceoptions-tenantid): String
```

## Properties<a name="aws-properties-ec2-verifiedaccesstrustprovider-deviceoptions-properties"></a>

`TenantId`  <a name="cfn-ec2-verifiedaccesstrustprovider-deviceoptions-tenantid"></a>
The ID of the tenant application with the device\-identity provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)