# AWS::S3::AccessPoint VpcConfiguration<a name="aws-properties-s3-accesspoint-vpcconfiguration"></a>

The Virtual Private Cloud \(VPC\) configuration for this access point\.

## Syntax<a name="aws-properties-s3-accesspoint-vpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-accesspoint-vpcconfiguration-syntax.json"></a>

```
{
  "[VpcId](#cfn-s3-accesspoint-vpcconfiguration-vpcid)" : String
}
```

### YAML<a name="aws-properties-s3-accesspoint-vpcconfiguration-syntax.yaml"></a>

```
  [VpcId](#cfn-s3-accesspoint-vpcconfiguration-vpcid): String
```

## Properties<a name="aws-properties-s3-accesspoint-vpcconfiguration-properties"></a>

`VpcId`  <a name="cfn-s3-accesspoint-vpcconfiguration-vpcid"></a>
If this field is specified, the access point will only allow connections from the specified VPC ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)