# AWS::MSK::Cluster ClientAuthentication<a name="aws-properties-msk-cluster-clientauthentication"></a>

Includes information related to client authentication\.

## Syntax<a name="aws-properties-msk-cluster-clientauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-clientauthentication-syntax.json"></a>

```
{
  "[Sasl](#cfn-msk-cluster-clientauthentication-sasl)" : Sasl,
  "[Tls](#cfn-msk-cluster-clientauthentication-tls)" : Tls,
  "[Unauthenticated](#cfn-msk-cluster-clientauthentication-unauthenticated)" : Unauthenticated
}
```

### YAML<a name="aws-properties-msk-cluster-clientauthentication-syntax.yaml"></a>

```
  [Sasl](#cfn-msk-cluster-clientauthentication-sasl): 
    Sasl
  [Tls](#cfn-msk-cluster-clientauthentication-tls): 
    Tls
  [Unauthenticated](#cfn-msk-cluster-clientauthentication-unauthenticated): 
    Unauthenticated
```

## Properties<a name="aws-properties-msk-cluster-clientauthentication-properties"></a>

`Sasl`  <a name="cfn-msk-cluster-clientauthentication-sasl"></a>
Details for ClientAuthentication using SASL\.  
*Required*: No  
*Type*: [Sasl](aws-properties-msk-cluster-sasl.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tls`  <a name="cfn-msk-cluster-clientauthentication-tls"></a>
Details for client authentication using TLS\.  
*Required*: No  
*Type*: [Tls](aws-properties-msk-cluster-tls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unauthenticated`  <a name="cfn-msk-cluster-clientauthentication-unauthenticated"></a>
Details for ClientAuthentication using no authentication\.  
*Required*: No  
*Type*: [Unauthenticated](aws-properties-msk-cluster-unauthenticated.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)