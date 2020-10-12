# AWS::MediaLive::Channel InputLocation<a name="aws-properties-medialive-channel-inputlocation"></a>

Contains the location and access credentials for data that is stored in an AWS service, when you need to use the password parameter from the EC2 parameter store\. This element is used by many elements in MediaLive\.

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
key used to extract the password from EC2 Parameter store\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-medialive-channel-inputlocation-uri"></a>
Uniform Resource Identifier \- This should be a path to a file accessible to the Live system \(eg\. a http:// URI\) depending on the output type\. For example, a RTMP destination should have a uri simliar to: "rtmp://fmsserver/live"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-medialive-channel-inputlocation-username"></a>
Username if credentials are required to access a file or publishing point\. This can be either a plaintext username, or a reference to an AWS parameter store name from which the username can be retrieved\. AWS Parameter store format: "ssm://<parameter name>"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)