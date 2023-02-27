# AWS::MSK::ServerlessCluster ClientAuthentication<a name="aws-properties-msk-serverlesscluster-clientauthentication"></a>

Includes all client authentication information\.

## Syntax<a name="aws-properties-msk-serverlesscluster-clientauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-serverlesscluster-clientauthentication-syntax.json"></a>

```
{
  "[Sasl](#cfn-msk-serverlesscluster-clientauthentication-sasl)" : Sasl
}
```

### YAML<a name="aws-properties-msk-serverlesscluster-clientauthentication-syntax.yaml"></a>

```
  [Sasl](#cfn-msk-serverlesscluster-clientauthentication-sasl): 
    Sasl
```

## Properties<a name="aws-properties-msk-serverlesscluster-clientauthentication-properties"></a>

`Sasl`  <a name="cfn-msk-serverlesscluster-clientauthentication-sasl"></a>
Details for client authentication using SASL\. To turn on SASL, you must also turn on `EncryptionInTransit` by setting `inCluster` to true\. You must set `clientBroker` to either `TLS` or `TLS_PLAINTEXT`\. If you choose `TLS_PLAINTEXT`, then you must also set `unauthenticated` to true\.  
*Required*: Yes  
*Type*: [Sasl](aws-properties-msk-serverlesscluster-sasl.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)