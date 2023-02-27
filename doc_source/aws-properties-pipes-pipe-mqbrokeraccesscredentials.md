# AWS::Pipes::Pipe MQBrokerAccessCredentials<a name="aws-properties-pipes-pipe-mqbrokeraccesscredentials"></a>

The AWS Secrets Manager secret that stores your broker credentials\.

## Syntax<a name="aws-properties-pipes-pipe-mqbrokeraccesscredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-mqbrokeraccesscredentials-syntax.json"></a>

```
{
  "[BasicAuth](#cfn-pipes-pipe-mqbrokeraccesscredentials-basicauth)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-mqbrokeraccesscredentials-syntax.yaml"></a>

```
  [BasicAuth](#cfn-pipes-pipe-mqbrokeraccesscredentials-basicauth): String
```

## Properties<a name="aws-properties-pipes-pipe-mqbrokeraccesscredentials-properties"></a>

`BasicAuth`  <a name="cfn-pipes-pipe-mqbrokeraccesscredentials-basicauth"></a>
The ARN of the Secrets Manager secret\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)