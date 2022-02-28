# AWS::MSK::BatchScramSecret UnprocessedScramSecret<a name="aws-properties-msk-batchscramsecret-unprocessedscramsecret"></a>

Error info for scram secret associate/disassociate failure\.

## Syntax<a name="aws-properties-msk-batchscramsecret-unprocessedscramsecret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-batchscramsecret-unprocessedscramsecret-syntax.json"></a>

```
{
  "[ErrorCode](#cfn-msk-batchscramsecret-unprocessedscramsecret-errorcode)" : String,
  "[ErrorMessage](#cfn-msk-batchscramsecret-unprocessedscramsecret-errormessage)" : String,
  "[SecretArn](#cfn-msk-batchscramsecret-unprocessedscramsecret-secretarn)" : String
}
```

### YAML<a name="aws-properties-msk-batchscramsecret-unprocessedscramsecret-syntax.yaml"></a>

```
  [ErrorCode](#cfn-msk-batchscramsecret-unprocessedscramsecret-errorcode): String
  [ErrorMessage](#cfn-msk-batchscramsecret-unprocessedscramsecret-errormessage): String
  [SecretArn](#cfn-msk-batchscramsecret-unprocessedscramsecret-secretarn): String
```

## Properties<a name="aws-properties-msk-batchscramsecret-unprocessedscramsecret-properties"></a>

`ErrorCode`  <a name="cfn-msk-batchscramsecret-unprocessedscramsecret-errorcode"></a>
Error code for associate/disassociate failure\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorMessage`  <a name="cfn-msk-batchscramsecret-unprocessedscramsecret-errormessage"></a>
Error message for associate/disassociate failure\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-msk-batchscramsecret-unprocessedscramsecret-secretarn"></a>
Amazon Secrets Manager secret ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)