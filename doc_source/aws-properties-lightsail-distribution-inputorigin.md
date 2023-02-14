# AWS::Lightsail::Distribution InputOrigin<a name="aws-properties-lightsail-distribution-inputorigin"></a>

`InputOrigin` is a property of the [AWS::Lightsail::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-distribution.html) resource\. It describes the origin resource of an Amazon Lightsail content delivery network \(CDN\) distribution\.

An origin can be a instance, bucket, or load balancer\. A distribution pulls content from an origin, caches it, and serves it to viewers through a worldwide network of edge servers\.

## Syntax<a name="aws-properties-lightsail-distribution-inputorigin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-inputorigin-syntax.json"></a>

```
{
  "[Name](#cfn-lightsail-distribution-inputorigin-name)" : String,
  "[ProtocolPolicy](#cfn-lightsail-distribution-inputorigin-protocolpolicy)" : String,
  "[RegionName](#cfn-lightsail-distribution-inputorigin-regionname)" : String
}
```

### YAML<a name="aws-properties-lightsail-distribution-inputorigin-syntax.yaml"></a>

```
  [Name](#cfn-lightsail-distribution-inputorigin-name): String
  [ProtocolPolicy](#cfn-lightsail-distribution-inputorigin-protocolpolicy): String
  [RegionName](#cfn-lightsail-distribution-inputorigin-regionname): String
```

## Properties<a name="aws-properties-lightsail-distribution-inputorigin-properties"></a>

`Name`  <a name="cfn-lightsail-distribution-inputorigin-name"></a>
The name of the origin resource\.  
*Required*: No  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtocolPolicy`  <a name="cfn-lightsail-distribution-inputorigin-protocolpolicy"></a>
The protocol that your Amazon Lightsail distribution uses when establishing a connection with your origin to pull content\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http-only | https-only`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionName`  <a name="cfn-lightsail-distribution-inputorigin-regionname"></a>
The AWS Region name of the origin resource\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ap-northeast-1 | ap-northeast-2 | ap-south-1 | ap-southeast-1 | ap-southeast-2 | ca-central-1 | eu-central-1 | eu-north-1 | eu-west-1 | eu-west-2 | eu-west-3 | us-east-1 | us-east-2 | us-west-1 | us-west-2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)