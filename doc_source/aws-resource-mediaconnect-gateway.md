# AWS::MediaConnect::Gateway<a name="aws-resource-mediaconnect-gateway"></a>

The AWS::MediaConnect::Gateway resource is used to create a new gateway\. AWS Elemental MediaConnect Gateway is a feature of MediaConnect that allows the deployment of on\-premises resources for transporting live video to and from the AWS Cloud\. MediaConnect Gateway allows you to contribute live video to the AWS Cloud from on\-premises hardware, as well as distribute live video from the AWS Cloud to your local data center\.

## Syntax<a name="aws-resource-mediaconnect-gateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-mediaconnect-gateway-syntax.json"></a>

```
{
  "Type" : "AWS::MediaConnect::Gateway",
  "Properties" : {
      "[EgressCidrBlocks](#cfn-mediaconnect-gateway-egresscidrblocks)" : [ String, ... ],
      "[Name](#cfn-mediaconnect-gateway-name)" : String,
      "[Networks](#cfn-mediaconnect-gateway-networks)" : [ GatewayNetwork, ... ]
    }
}
```

### YAML<a name="aws-resource-mediaconnect-gateway-syntax.yaml"></a>

```
Type: AWS::MediaConnect::Gateway
Properties: 
  [EgressCidrBlocks](#cfn-mediaconnect-gateway-egresscidrblocks): 
    - String
  [Name](#cfn-mediaconnect-gateway-name): String
  [Networks](#cfn-mediaconnect-gateway-networks): 
    - GatewayNetwork
```

## Properties<a name="aws-resource-mediaconnect-gateway-properties"></a>

`EgressCidrBlocks`  <a name="cfn-mediaconnect-gateway-egresscidrblocks"></a>
The range of IP addresses that are allowed to contribute content or initiate output requests for flows communicating with this gateway\. These IP addresses should be in the form of a Classless Inter\-Domain Routing \(CIDR\) block; for example, 10\.0\.0\.0/16\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-mediaconnect-gateway-name"></a>
The name of the gateway\. This name can not be modified after the gateway is created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Networks`  <a name="cfn-mediaconnect-gateway-networks"></a>
The list of networks that you want to add\.  
*Required*: Yes  
*Type*: List of [GatewayNetwork](aws-properties-mediaconnect-gateway-gatewaynetwork.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-mediaconnect-gateway-return-values"></a>

### Ref<a name="aws-resource-mediaconnect-gateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the gateway ARN\. For example:

`{ "Ref": "arn:aws:mediaconnect:us-east-1:111122223333:gateway:1-23aBC45dEF67hiJ8-12AbC34DE5fG:WestOffice" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-mediaconnect-gateway-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-mediaconnect-gateway-return-values-fn--getatt-fn--getatt"></a>

`GatewayArn`  <a name="GatewayArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the gateway\.

`GatewayState`  <a name="GatewayState-fn::getatt"></a>
The current state of the gateway\. Possible values are: CREATING, ACTIVE, UPDATING, ERROR, DELETING, DELETED\.