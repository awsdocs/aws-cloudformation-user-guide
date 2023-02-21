# AWS::MSK::ServerlessCluster Sasl<a name="aws-properties-msk-serverlesscluster-sasl"></a>

Details for client authentication using SASL\. To turn on SASL, you must also turn on `EncryptionInTransit` by setting `inCluster` to true\. You must set `clientBroker` to either `TLS` or `TLS_PLAINTEXT`\. If you choose `TLS_PLAINTEXT`, then you must also set `unauthenticated` to true\.

## Syntax<a name="aws-properties-msk-serverlesscluster-sasl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-serverlesscluster-sasl-syntax.json"></a>

```
{
  "[Iam](#cfn-msk-serverlesscluster-sasl-iam)" : Iam
}
```

### YAML<a name="aws-properties-msk-serverlesscluster-sasl-syntax.yaml"></a>

```
  [Iam](#cfn-msk-serverlesscluster-sasl-iam): 
    Iam
```

## Properties<a name="aws-properties-msk-serverlesscluster-sasl-properties"></a>

`Iam`  <a name="cfn-msk-serverlesscluster-sasl-iam"></a>
Details for client authentication using IAM\.  
*Required*: Yes  
*Type*: [Iam](aws-properties-msk-serverlesscluster-iam.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)