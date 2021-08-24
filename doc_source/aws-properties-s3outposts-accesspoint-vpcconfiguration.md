# AWS::S3Outposts::AccessPoint VpcConfiguration<a name="aws-properties-s3outposts-accesspoint-vpcconfiguration"></a>

Contains the virtual private cloud \(VPC\) configuration for the specified access point\.

## Syntax<a name="aws-properties-s3outposts-accesspoint-vpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3outposts-accesspoint-vpcconfiguration-syntax.json"></a>

```
{
  "[VpcId](#cfn-s3outposts-accesspoint-vpcconfiguration-vpcid)" : String
}
```

### YAML<a name="aws-properties-s3outposts-accesspoint-vpcconfiguration-syntax.yaml"></a>

```
  [VpcId](#cfn-s3outposts-accesspoint-vpcconfiguration-vpcid): String
```

## Properties<a name="aws-properties-s3outposts-accesspoint-vpcconfiguration-properties"></a>

`VpcId`  <a name="cfn-s3outposts-accesspoint-vpcconfiguration-vpcid"></a>
The ID of the VPC configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)