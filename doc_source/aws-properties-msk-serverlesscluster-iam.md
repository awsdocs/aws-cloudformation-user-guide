# AWS::MSK::ServerlessCluster Iam<a name="aws-properties-msk-serverlesscluster-iam"></a>

Details for IAM client authentication\.

## Syntax<a name="aws-properties-msk-serverlesscluster-iam-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-serverlesscluster-iam-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-serverlesscluster-iam-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-msk-serverlesscluster-iam-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-serverlesscluster-iam-enabled): Boolean
```

## Properties<a name="aws-properties-msk-serverlesscluster-iam-properties"></a>

`Enabled`  <a name="cfn-msk-serverlesscluster-iam-enabled"></a>
SASL/IAM authentication is enabled or not\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)