# AWS::Glue::Job NotificationProperty<a name="aws-properties-glue-job-notificationproperty"></a>

Specifies configuration properties of a notification\.

## Syntax<a name="aws-properties-glue-job-notificationproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-notificationproperty-syntax.json"></a>

```
{
  "[NotifyDelayAfter](#cfn-glue-job-notificationproperty-notifydelayafter)" : Integer
}
```

### YAML<a name="aws-properties-glue-job-notificationproperty-syntax.yaml"></a>

```
  [NotifyDelayAfter](#cfn-glue-job-notificationproperty-notifydelayafter): Integer
```

## Properties<a name="aws-properties-glue-job-notificationproperty-properties"></a>

`NotifyDelayAfter`  <a name="cfn-glue-job-notificationproperty-notifydelayafter"></a>
After a job run starts, the number of minutes to wait before sending a job run delay notification\.  
*Required*: No  
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
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
