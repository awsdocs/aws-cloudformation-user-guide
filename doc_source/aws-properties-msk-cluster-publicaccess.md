# AWS::MSK::Cluster PublicAccess<a name="aws-properties-msk-cluster-publicaccess"></a>

Specifies whether the cluster's brokers are accessible from the internet\. Public access is off by default\.

## Syntax<a name="aws-properties-msk-cluster-publicaccess-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-publicaccess-syntax.json"></a>

```
{
  "[Type](#cfn-msk-cluster-publicaccess-type)" : String
}
```

### YAML<a name="aws-properties-msk-cluster-publicaccess-syntax.yaml"></a>

```
  [Type](#cfn-msk-cluster-publicaccess-type): String
```

## Properties<a name="aws-properties-msk-cluster-publicaccess-properties"></a>

`Type`  <a name="cfn-msk-cluster-publicaccess-type"></a>
Set to `DISABLED` to turn off public access or to `SERVICE_PROVIDED_EIPS` to turn it on\. Public access if off by default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)