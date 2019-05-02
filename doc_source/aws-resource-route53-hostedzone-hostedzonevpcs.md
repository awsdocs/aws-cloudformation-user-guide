# AWS::Route53::HostedZone VPC<a name="aws-resource-route53-hostedzone-hostedzonevpcs"></a>

\(Private hosted zones only\) A complex type that contains information about an Amazon VPC\.

## Syntax<a name="aws-resource-route53-hostedzone-hostedzonevpcs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-hostedzone-hostedzonevpcs-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::HostedZone",
  "Properties" : {  
    "[VPCId](#cfn-route53-hostedzone-hostedzonevpcs-vpcid)" : String,
    "[VPCRegion](#cfn-route53-hostedzone-hostedzonevpcs-vpcregion)" : String
}
```

### YAML<a name="aws-resource-route53-hostedzone-hostedzonevpcs-syntax.yaml"></a>

```
  Type: "AWS::Route53::HostedZone"
  Properties: 
    [VPCId](#cfn-route53-hostedzone-hostedzonevpcs-vpcid) : String
    [VPCRegion](#cfn-route53-hostedzone-hostedzonevpcs-vpcregion) : String
```

## Properties<a name="aws-resource-route53-hostedzone-hostedzonevpcs-properties"></a>

`VPCId`  <a name="cfn-route53-hostedzone-hostedzonevpcs-vpcid"></a>
\(Private hosted zones only\) The ID of an Amazon VPC\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCRegion`  <a name="cfn-route53-hostedzone-hostedzonevpcs-vpcregion"></a>
\(Private hosted zones only\) The region that an Amazon VPC was created in\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `ap-northeast-1 | ap-northeast-2 | ap-northeast-3 | ap-south-1 | ap-southeast-1 | ap-southeast-2 | ca-central-1 | cn-north-1 | eu-central-1 | eu-north-1 | eu-west-1 | eu-west-2 | eu-west-3 | sa-east-1 | us-east-1 | us-east-2 | us-west-1 | us-west-2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-resource-route53-hostedzone-hostedzonevpcs--seealso"></a>
+  [VPC](https://docs.aws.amazon.com/Route53/latest/APIReference/API_VPC.html) in the *Amazon Route 53 API Reference* 
