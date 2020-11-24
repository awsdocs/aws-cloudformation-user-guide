# AWS::MediaLive::Input InputDestinationRequest<a name="aws-properties-medialive-input-inputdestinationrequest"></a>

Endpoint settings for a PUSH type input\.

## Syntax<a name="aws-properties-medialive-input-inputdestinationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-input-inputdestinationrequest-syntax.json"></a>

```
{
  "[StreamName](#cfn-medialive-input-inputdestinationrequest-streamname)" : String
}
```

### YAML<a name="aws-properties-medialive-input-inputdestinationrequest-syntax.yaml"></a>

```
  [StreamName](#cfn-medialive-input-inputdestinationrequest-streamname): String
```

## Properties<a name="aws-properties-medialive-input-inputdestinationrequest-properties"></a>

`StreamName`  <a name="cfn-medialive-input-inputdestinationrequest-streamname"></a>
A unique name for the location the RTMP stream is being pushed to\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)