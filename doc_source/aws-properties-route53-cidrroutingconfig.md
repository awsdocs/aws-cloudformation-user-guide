# AWS::Route53::RecordSetGroup CidrRoutingConfig<a name="aws-properties-route53-cidrroutingconfig"></a>

The object that is specified in resource record set object when you are linking a resource record set to a CIDR location\.

A `LocationName` with an asterisk “\*” can be used to create a default CIDR record\. `CollectionId` is still required for default record\.

## Syntax<a name="aws-properties-route53-cidrroutingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-cidrroutingconfig-syntax.json"></a>

```
{
  "[CollectionId](#cfn-route53-cidrroutingconfig-collectionid)" : String,
  "[LocationName](#cfn-route53-cidrroutingconfig-locationname)" : String
}
```

### YAML<a name="aws-properties-route53-cidrroutingconfig-syntax.yaml"></a>

```
  [CollectionId](#cfn-route53-cidrroutingconfig-collectionid): String
  [LocationName](#cfn-route53-cidrroutingconfig-locationname): String
```

## Properties<a name="aws-properties-route53-cidrroutingconfig-properties"></a>

`CollectionId`  <a name="cfn-route53-cidrroutingconfig-collectionid"></a>
The CIDR collection ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[0-9a-f]{8}-(?:[0-9a-f]{4}-){3}[0-9a-f]{12}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocationName`  <a name="cfn-route53-cidrroutingconfig-locationname"></a>
The CIDR collection location name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16`  
*Pattern*: `[0-9A-Za-z_\-\*]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)