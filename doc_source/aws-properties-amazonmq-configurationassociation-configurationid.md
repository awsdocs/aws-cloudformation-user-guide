# AWS::AmazonMQ::ConfigurationAssociation ConfigurationId<a name="aws-properties-amazonmq-configurationassociation-configurationid"></a>

The `ConfigurationId` property type specifies a configuration Id and the revision of a configuration\.

## Syntax<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax.json"></a>

```
{
  "[Id](#cfn-amazonmq-configurationassociation-configurationid-id)" : String,
  "[Revision](#cfn-amazonmq-configurationassociation-configurationid-revision)" : Integer
}
```

### YAML<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax.yaml"></a>

```
  [Id](#cfn-amazonmq-configurationassociation-configurationid-id): String
  [Revision](#cfn-amazonmq-configurationassociation-configurationid-revision): Integer
```

## Properties<a name="aws-properties-amazonmq-configurationassociation-configurationid-properties"></a>

`Id`  <a name="cfn-amazonmq-configurationassociation-configurationid-id"></a>
The unique ID that Amazon MQ generates for the configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-amazonmq-configurationassociation-configurationid-revision"></a>
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
