# AWS::DeviceFarm::NetworkProfile<a name="aws-resource-devicefarm-networkprofile"></a>

Creates a network profile\.

## Syntax<a name="aws-resource-devicefarm-networkprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devicefarm-networkprofile-syntax.json"></a>

```
{
  "Type" : "AWS::DeviceFarm::NetworkProfile",
  "Properties" : {
      "[Description](#cfn-devicefarm-networkprofile-description)" : String,
      "[DownlinkBandwidthBits](#cfn-devicefarm-networkprofile-downlinkbandwidthbits)" : Integer,
      "[DownlinkDelayMs](#cfn-devicefarm-networkprofile-downlinkdelayms)" : Integer,
      "[DownlinkJitterMs](#cfn-devicefarm-networkprofile-downlinkjitterms)" : Integer,
      "[DownlinkLossPercent](#cfn-devicefarm-networkprofile-downlinklosspercent)" : Integer,
      "[Name](#cfn-devicefarm-networkprofile-name)" : String,
      "[ProjectArn](#cfn-devicefarm-networkprofile-projectarn)" : String,
      "[Tags](#cfn-devicefarm-networkprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UplinkBandwidthBits](#cfn-devicefarm-networkprofile-uplinkbandwidthbits)" : Integer,
      "[UplinkDelayMs](#cfn-devicefarm-networkprofile-uplinkdelayms)" : Integer,
      "[UplinkJitterMs](#cfn-devicefarm-networkprofile-uplinkjitterms)" : Integer,
      "[UplinkLossPercent](#cfn-devicefarm-networkprofile-uplinklosspercent)" : Integer
    }
}
```

### YAML<a name="aws-resource-devicefarm-networkprofile-syntax.yaml"></a>

```
Type: AWS::DeviceFarm::NetworkProfile
Properties: 
  [Description](#cfn-devicefarm-networkprofile-description): String
  [DownlinkBandwidthBits](#cfn-devicefarm-networkprofile-downlinkbandwidthbits): Integer
  [DownlinkDelayMs](#cfn-devicefarm-networkprofile-downlinkdelayms): Integer
  [DownlinkJitterMs](#cfn-devicefarm-networkprofile-downlinkjitterms): Integer
  [DownlinkLossPercent](#cfn-devicefarm-networkprofile-downlinklosspercent): Integer
  [Name](#cfn-devicefarm-networkprofile-name): String
  [ProjectArn](#cfn-devicefarm-networkprofile-projectarn): String
  [Tags](#cfn-devicefarm-networkprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UplinkBandwidthBits](#cfn-devicefarm-networkprofile-uplinkbandwidthbits): Integer
  [UplinkDelayMs](#cfn-devicefarm-networkprofile-uplinkdelayms): Integer
  [UplinkJitterMs](#cfn-devicefarm-networkprofile-uplinkjitterms): Integer
  [UplinkLossPercent](#cfn-devicefarm-networkprofile-uplinklosspercent): Integer
```

## Properties<a name="aws-resource-devicefarm-networkprofile-properties"></a>

`Description`  <a name="cfn-devicefarm-networkprofile-description"></a>
The description of the network profile\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16384`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DownlinkBandwidthBits`  <a name="cfn-devicefarm-networkprofile-downlinkbandwidthbits"></a>
The data throughput rate in bits per second, as an integer from 0 to 104857600\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DownlinkDelayMs`  <a name="cfn-devicefarm-networkprofile-downlinkdelayms"></a>
Delay time for all packets to destination in milliseconds as an integer from 0 to 2000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DownlinkJitterMs`  <a name="cfn-devicefarm-networkprofile-downlinkjitterms"></a>
Time variation in the delay of received packets in milliseconds as an integer from 0 to 2000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DownlinkLossPercent`  <a name="cfn-devicefarm-networkprofile-downlinklosspercent"></a>
Proportion of received packets that fail to arrive from 0 to 100 percent\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-devicefarm-networkprofile-name"></a>
The name of the network profile\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProjectArn`  <a name="cfn-devicefarm-networkprofile-projectarn"></a>
The Amazon Resource Name \(ARN\) of the specified project\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-devicefarm-networkprofile-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation resource type reference guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UplinkBandwidthBits`  <a name="cfn-devicefarm-networkprofile-uplinkbandwidthbits"></a>
The data throughput rate in bits per second, as an integer from 0 to 104857600\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UplinkDelayMs`  <a name="cfn-devicefarm-networkprofile-uplinkdelayms"></a>
Delay time for all packets to destination in milliseconds as an integer from 0 to 2000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UplinkJitterMs`  <a name="cfn-devicefarm-networkprofile-uplinkjitterms"></a>
Time variation in the delay of received packets in milliseconds as an integer from 0 to 2000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UplinkLossPercent`  <a name="cfn-devicefarm-networkprofile-uplinklosspercent"></a>
Proportion of transmitted packets that fail to arrive from 0 to 100 percent\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-devicefarm-networkprofile-return-values"></a>

### Ref<a name="aws-resource-devicefarm-networkprofile-return-values-ref"></a>

Not supported for this resource\.

### Fn::GetAtt<a name="aws-resource-devicefarm-networkprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-devicefarm-networkprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the network profile\. See [Amazon resource names](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *General Reference guide*\.