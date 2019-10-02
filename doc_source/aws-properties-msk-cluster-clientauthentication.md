# AWS::MSK::Cluster ClientAuthentication<a name="aws-properties-msk-cluster-clientauthentication"></a>

Includes information related to client authentication\.

## Syntax<a name="aws-properties-msk-cluster-clientauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-clientauthentication-syntax.json"></a>

```
{
  "[Tls](#cfn-msk-cluster-clientauthentication-tls)" : [Tls](aws-properties-msk-cluster-tls.md)
}
```

### YAML<a name="aws-properties-msk-cluster-clientauthentication-syntax.yaml"></a>

```
  [Tls](#cfn-msk-cluster-clientauthentication-tls): 
    [Tls](aws-properties-msk-cluster-tls.md)
```

## Properties<a name="aws-properties-msk-cluster-clientauthentication-properties"></a>

`Tls`  <a name="cfn-msk-cluster-clientauthentication-tls"></a>
Details for client authentication using TLS\.  
*Required*: No  
*Type*: [Tls](aws-properties-msk-cluster-tls.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-2`
