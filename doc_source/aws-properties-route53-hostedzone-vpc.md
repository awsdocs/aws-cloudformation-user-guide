# AWS::Route53::HostedZone VPC<a name="aws-properties-route53-hostedzone-vpc"></a>

*Private hosted zones only:* A complex type that contains information about an Amazon VPC\. Route 53 Resolver uses the records in the private hosted zone to route traffic in that VPC\. 

**Note**  
For public hosted zones, omit `VPCs`, `VPCId`, and `VPCRegion`\.

## Syntax<a name="aws-properties-route53-hostedzone-vpc-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-hostedzone-vpc-syntax.json"></a>

```
{
  "[VPCId](#cfn-route53-hostedzone-vpc-vpcid)" : String,
  "[VPCRegion](#cfn-route53-hostedzone-vpc-vpcregion)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-vpc-syntax.yaml"></a>

```
  [VPCId](#cfn-route53-hostedzone-vpc-vpcid): String
  [VPCRegion](#cfn-route53-hostedzone-vpc-vpcregion): String
```

## Properties<a name="aws-properties-route53-hostedzone-vpc-properties"></a>

`VPCId`  <a name="cfn-route53-hostedzone-vpc-vpcid"></a>
*Private hosted zones only:* The ID of an Amazon VPC\.  
For public hosted zones, omit `VPCs`, `VPCId`, and `VPCRegion`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCRegion`  <a name="cfn-route53-hostedzone-vpc-vpcregion"></a>
*Private hosted zones only:* The region that an Amazon VPC was created in\.  
For public hosted zones, omit `VPCs`, `VPCId`, and `VPCRegion`\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `af-south-1 | ap-east-1 | ap-northeast-1 | ap-northeast-2 | ap-northeast-3 | ap-south-1 | ap-southeast-1 | ap-southeast-2 | ca-central-1 | cn-north-1 | eu-central-1 | eu-north-1 | eu-south-1 | eu-west-1 | eu-west-2 | eu-west-3 | me-south-1 | sa-east-1 | us-east-1 | us-east-2 | us-gov-east-1 | us-gov-west-1 | us-iso-east-1 | us-isob-east-1 | us-west-1 | us-west-2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-hostedzone-vpc--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html#aws-resource-route53-hostedzone-return-values) in the topic [AWS::Route53::HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html) 
+  [VPC](https://docs.aws.amazon.com/Route53/latest/APIReference/API_VPC.html) in the *Amazon Route 53 API Reference* 

