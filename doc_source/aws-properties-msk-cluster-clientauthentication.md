# AWS::MSK::Cluster ClientAuthentication<a name="aws-properties-msk-cluster-clientauthentication"></a>

Includes information related to client authentication\.

## Syntax<a name="aws-properties-msk-cluster-clientauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-clientauthentication-syntax.json"></a>

```
{
  "[Tls](#cfn-msk-cluster-clientauthentication-tls)" : Tls
}
```

### YAML<a name="aws-properties-msk-cluster-clientauthentication-syntax.yaml"></a>

```
  [Tls](#cfn-msk-cluster-clientauthentication-tls): 
    Tls
```

## Properties<a name="aws-properties-msk-cluster-clientauthentication-properties"></a>

`Tls`  <a name="cfn-msk-cluster-clientauthentication-tls"></a>
Details for client authentication using TLS\.  
*Required*: No  
*Type*: [Tls](aws-properties-msk-cluster-tls.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)