# AWS::MSK::Cluster ConfigurationInfo<a name="aws-properties-msk-cluster-configurationinfo"></a>

Specifies the Amazon MSK configuration to use for the brokers\.

## Syntax<a name="aws-properties-msk-cluster-configurationinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-configurationinfo-syntax.json"></a>

```
{
  "[Arn](#cfn-msk-cluster-configurationinfo-arn)" : String,
  "[Revision](#cfn-msk-cluster-configurationinfo-revision)" : Integer
}
```

### YAML<a name="aws-properties-msk-cluster-configurationinfo-syntax.yaml"></a>

```
  [Arn](#cfn-msk-cluster-configurationinfo-arn): String
  [Revision](#cfn-msk-cluster-configurationinfo-revision): Integer
```

## Properties<a name="aws-properties-msk-cluster-configurationinfo-properties"></a>

`Arn`  <a name="cfn-msk-cluster-configurationinfo-arn"></a>
The Amazon Resource Name \(ARN\) of the MSK configuration to use\. For example, `arn:aws:kafka:us-east-1:123456789012:configuration/example-configuration-name/abcdabcd-1234-abcd-1234-abcd123e8e8e-1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-msk-cluster-configurationinfo-revision"></a>
The revision of the Amazon MSK configuration to use\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)