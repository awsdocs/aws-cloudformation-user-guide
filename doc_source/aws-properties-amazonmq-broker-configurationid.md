# AWS::AmazonMQ::Broker ConfigurationId<a name="aws-properties-amazonmq-broker-configurationid"></a>

A list of information about the configuration\.

## Syntax<a name="aws-properties-amazonmq-broker-configurationid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-configurationid-syntax.json"></a>

```
{
  "[Id](#cfn-amazonmq-broker-configurationid-id)" : String,
  "[Revision](#cfn-amazonmq-broker-configurationid-revision)" : Integer
}
```

### YAML<a name="aws-properties-amazonmq-broker-configurationid-syntax.yaml"></a>

```
  [Id](#cfn-amazonmq-broker-configurationid-id): String
  [Revision](#cfn-amazonmq-broker-configurationid-revision): Integer
```

## Properties<a name="aws-properties-amazonmq-broker-configurationid-properties"></a>

`Id`  <a name="cfn-amazonmq-broker-configurationid-id"></a>
The unique ID that Amazon MQ generates for the configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-amazonmq-broker-configurationid-revision"></a>
The revision number of the configuration\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
