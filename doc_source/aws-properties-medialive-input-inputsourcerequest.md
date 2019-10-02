# AWS::MediaLive::Input InputSourceRequest<a name="aws-properties-medialive-input-inputsourcerequest"></a>

The settings for a pull input\.

## Syntax<a name="aws-properties-medialive-input-inputsourcerequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-input-inputsourcerequest-syntax.json"></a>

```
{
  "[PasswordParam](#cfn-medialive-input-inputsourcerequest-passwordparam)" : String,
  "[Url](#cfn-medialive-input-inputsourcerequest-url)" : String,
  "[Username](#cfn-medialive-input-inputsourcerequest-username)" : String
}
```

### YAML<a name="aws-properties-medialive-input-inputsourcerequest-syntax.yaml"></a>

```
  [PasswordParam](#cfn-medialive-input-inputsourcerequest-passwordparam): String
  [Url](#cfn-medialive-input-inputsourcerequest-url): String
  [Username](#cfn-medialive-input-inputsourcerequest-username): String
```

## Properties<a name="aws-properties-medialive-input-inputsourcerequest-properties"></a>

`PasswordParam`  <a name="cfn-medialive-input-inputsourcerequest-passwordparam"></a>
The password parameter that holds the password for accessing the upstream system\. The password parameter applies only if the upstream system requires credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-medialive-input-inputsourcerequest-url"></a>
For a pull input, the URL where MediaLive pulls the source content from\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-medialive-input-inputsourcerequest-username"></a>
The user name for accessing the upstream system\. The user name applies only if the upstream system requires credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `sa-east-1`
- `us-east-1`
- `us-west-2`
