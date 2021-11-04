# AWS::MediaLive::Channel CdiInputSpecification<a name="aws-properties-medialive-channel-cdiinputspecification"></a>

The input specification for this channel\. It specifies the key characteristics of CDI inputs for this channel, when those characteristics are different from other inputs\. 

This entity is at the top level in the channel\.

## Syntax<a name="aws-properties-medialive-channel-cdiinputspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-cdiinputspecification-syntax.json"></a>

```
{
  "[Resolution](#cfn-medialive-channel-cdiinputspecification-resolution)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-cdiinputspecification-syntax.yaml"></a>

```
  [Resolution](#cfn-medialive-channel-cdiinputspecification-resolution): String
```

## Properties<a name="aws-properties-medialive-channel-cdiinputspecification-properties"></a>

`Resolution`  <a name="cfn-medialive-channel-cdiinputspecification-resolution"></a>
Maximum CDI input resolution  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)