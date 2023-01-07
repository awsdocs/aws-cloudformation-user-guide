# AWS::MediaLive::Input InputDestinationRequest<a name="aws-properties-medialive-input-inputdestinationrequest"></a>

Settings that apply only if the input is a push type of input\.

The parent of this entity is Input\.

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
The stream name \(application name/application instance\) for the location the RTMP source content will be pushed to in MediaLive\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)