# Route 53 HostedZoneVPCs<a name="aws-resource-route53-hostedzone-hostedzonevpcs"></a>

The `HostedZoneVPCs` property is part of the [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md) resource that specifies the VPCs to associate with the hosted zone\.

## Syntax<a name="w3ab2c21c14e1673b5"></a>

### JSON<a name="aws-properties-route53-hostedzone-hostedzonevpcs-syntax.json"></a>

```
{
  "[VPCId](#cfn-route53-hostedzone-hostedzonevpcs-vpcid)" : String,
  "[VPCRegion](#cfn-route53-hostedzone-hostedzonevpcs-vpcregion)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-hostedzonevpcs-syntax.yaml"></a>

```
[VPCId](#cfn-route53-hostedzone-hostedzonevpcs-vpcid): String
[VPCRegion](#cfn-route53-hostedzone-hostedzonevpcs-vpcregion): String
```

## Properties<a name="w3ab2c21c14e1673b7"></a>

`VPCId`  <a name="cfn-route53-hostedzone-hostedzonevpcs-vpcid"></a>
The ID of the Amazon VPC that you want to associate with the hosted zone\.  
*Required*: Yes  
*Type*: String

`VPCRegion`  <a name="cfn-route53-hostedzone-hostedzonevpcs-vpcregion"></a>
The region in which the Amazon VPC was created as specified in the `VPCId` property\.  
*Required*: Yes  
*Type*: String