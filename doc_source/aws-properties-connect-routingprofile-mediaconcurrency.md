# AWS::Connect::RoutingProfile MediaConcurrency<a name="aws-properties-connect-routingprofile-mediaconcurrency"></a>

Contains information about which channels are supported, and how many contacts an agent can have on a channel simultaneously\.

## Syntax<a name="aws-properties-connect-routingprofile-mediaconcurrency-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-routingprofile-mediaconcurrency-syntax.json"></a>

```
{
  "[Channel](#cfn-connect-routingprofile-mediaconcurrency-channel)" : String,
  "[Concurrency](#cfn-connect-routingprofile-mediaconcurrency-concurrency)" : Integer,
  "[CrossChannelBehavior](#cfn-connect-routingprofile-mediaconcurrency-crosschannelbehavior)" : CrossChannelBehavior
}
```

### YAML<a name="aws-properties-connect-routingprofile-mediaconcurrency-syntax.yaml"></a>

```
  [Channel](#cfn-connect-routingprofile-mediaconcurrency-channel): String
  [Concurrency](#cfn-connect-routingprofile-mediaconcurrency-concurrency): Integer
  [CrossChannelBehavior](#cfn-connect-routingprofile-mediaconcurrency-crosschannelbehavior): 
    CrossChannelBehavior
```

## Properties<a name="aws-properties-connect-routingprofile-mediaconcurrency-properties"></a>

`Channel`  <a name="cfn-connect-routingprofile-mediaconcurrency-channel"></a>
The channels that agents can handle in the Contact Control Panel \(CCP\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CHAT | TASK | VOICE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Concurrency`  <a name="cfn-connect-routingprofile-mediaconcurrency-concurrency"></a>
The number of contacts an agent can have on a channel simultaneously\.  
Valid Range for `VOICE`: Minimum value of 1\. Maximum value of 1\.  
Valid Range for `CHAT`: Minimum value of 1\. Maximum value of 10\.  
Valid Range for `TASK`: Minimum value of 1\. Maximum value of 10\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrossChannelBehavior`  <a name="cfn-connect-routingprofile-mediaconcurrency-crosschannelbehavior"></a>
Defines the cross\-channel routing behavior for each channel that is enabled for this Routing Profile\. For example, this allows you to offer an agent a different contact from another channel when they are currently working with a contact from a Voice channel\.  
*Required*: No  
*Type*: [CrossChannelBehavior](aws-properties-connect-routingprofile-crosschannelbehavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)