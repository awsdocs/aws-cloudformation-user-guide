# AWS::MediaLive::Channel InputLocation<a name="aws-properties-medialive-channel-inputlocation"></a>

The input location\.

The parent of this entity is InputLossBehavior\.

## Syntax<a name="aws-properties-medialive-channel-inputlocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputlocation-syntax.json"></a>

```
{
  "[PasswordParam](#cfn-medialive-channel-inputlocation-passwordparam)" : String,
  "[Uri](#cfn-medialive-channel-inputlocation-uri)" : String,
  "[Username](#cfn-medialive-channel-inputlocation-username)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-inputlocation-syntax.yaml"></a>

```
  [PasswordParam](#cfn-medialive-channel-inputlocation-passwordparam): String
  [Uri](#cfn-medialive-channel-inputlocation-uri): String
  [Username](#cfn-medialive-channel-inputlocation-username): String
```

## Properties<a name="aws-properties-medialive-channel-inputlocation-properties"></a>

`PasswordParam`  <a name="cfn-medialive-channel-inputlocation-passwordparam"></a>
The password parameter that holds the password for accessing the downstream system\. This applies only if the downstream system requires credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-medialive-channel-inputlocation-uri"></a>
The URI should be a path to a file that is accessible to the Live system \(for example, an http:// URI\) depending on the output type\. For example, an RTMP destination should have a URI similar to rtmp://fmsserver/live\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-medialive-channel-inputlocation-username"></a>
The user name for accessing the downstream system\. This applies only if the downstream system requires credentials\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)