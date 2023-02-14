# AWS::IoTWireless::PartnerAccount<a name="aws-resource-iotwireless-partneraccount"></a>

A partner account\. If `PartnerAccountId` and `PartnerType` are `null`, returns all partner accounts\.

## Syntax<a name="aws-resource-iotwireless-partneraccount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-partneraccount-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::PartnerAccount",
  "Properties" : {
      "[PartnerAccountId](#cfn-iotwireless-partneraccount-partneraccountid)" : String,
      "[Sidewalk](#cfn-iotwireless-partneraccount-sidewalk)" : SidewalkAccountInfo,
      "[Tags](#cfn-iotwireless-partneraccount-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-partneraccount-syntax.yaml"></a>

```
Type: AWS::IoTWireless::PartnerAccount
Properties: 
  [PartnerAccountId](#cfn-iotwireless-partneraccount-partneraccountid): String
  [Sidewalk](#cfn-iotwireless-partneraccount-sidewalk): 
    SidewalkAccountInfo
  [Tags](#cfn-iotwireless-partneraccount-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-partneraccount-properties"></a>

`PartnerAccountId`  <a name="cfn-iotwireless-partneraccount-partneraccountid"></a>
The ID of the partner account to update\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Sidewalk`  <a name="cfn-iotwireless-partneraccount-sidewalk"></a>
The Sidewalk account credentials\.  
*Required*: No  
*Type*: [SidewalkAccountInfo](aws-properties-iotwireless-partneraccount-sidewalkaccountinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-partneraccount-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-partneraccount-return-values"></a>

### Ref<a name="aws-resource-iotwireless-partneraccount-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the partner account\.

### Fn::GetAtt<a name="aws-resource-iotwireless-partneraccount-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-partneraccount-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resource\.

`SidewalkResponse`  <a name="SidewalkResponse-fn::getatt"></a>
The Sidewalk account credentials\.