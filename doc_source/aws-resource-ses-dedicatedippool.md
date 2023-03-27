# AWS::SES::DedicatedIpPool<a name="aws-resource-ses-dedicatedippool"></a>

Create a new pool of dedicated IP addresses\. A pool can include one or more dedicated IP addresses that are associated with your AWS account\. You can associate a pool with a configuration set\. When you send an email that uses that configuration set, the message is sent from one of the addresses in the associated pool\.

**Important**  
You can't delete dedicated IP pools that have a `STANDARD` scaling mode and one or more dedicated IP addresses\. This constraint doesn't apply to dedicated IP pools that have a `MANAGED` scaling mode\.

## Syntax<a name="aws-resource-ses-dedicatedippool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ses-dedicatedippool-syntax.json"></a>

```
{
  "Type" : "AWS::SES::DedicatedIpPool",
  "Properties" : {
      "[PoolName](#cfn-ses-dedicatedippool-poolname)" : String,
      "[ScalingMode](#cfn-ses-dedicatedippool-scalingmode)" : String
    }
}
```

### YAML<a name="aws-resource-ses-dedicatedippool-syntax.yaml"></a>

```
Type: AWS::SES::DedicatedIpPool
Properties: 
  [PoolName](#cfn-ses-dedicatedippool-poolname): String
  [ScalingMode](#cfn-ses-dedicatedippool-scalingmode): String
```

## Properties<a name="aws-resource-ses-dedicatedippool-properties"></a>

`PoolName`  <a name="cfn-ses-dedicatedippool-poolname"></a>
The name of the dedicated IP pool that the IP address is associated with\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingMode`  <a name="cfn-ses-dedicatedippool-scalingmode"></a>
The type of scaling mode\.  
The following options are available:  
+ `STANDARD` \- The customer controls which IPs are part of the dedicated IP pool\.
+ `MANAGED` \- The reputation and number of IPs is automatically managed by Amazon SES\.
The `STANDARD` option is selected by default if no value is specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ses-dedicatedippool-return-values"></a>

### Ref<a name="aws-resource-ses-dedicatedippool-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.