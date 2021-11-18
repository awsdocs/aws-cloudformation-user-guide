# AWS::Route53RecoveryReadiness::ResourceSet DNSTargetResource<a name="aws-properties-route53recoveryreadiness-resourceset-dnstargetresource"></a>

A component for DNS/routing control readiness checks and architecture checks\.

## Syntax<a name="aws-properties-route53recoveryreadiness-resourceset-dnstargetresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoveryreadiness-resourceset-dnstargetresource-syntax.json"></a>

```
{
  "[DomainName](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-domainname)" : String,
  "[HostedZoneArn](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-hostedzonearn)" : String,
  "[RecordSetId](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordsetid)" : String,
  "[RecordType](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordtype)" : String,
  "[TargetResource](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-targetresource)" : TargetResource
}
```

### YAML<a name="aws-properties-route53recoveryreadiness-resourceset-dnstargetresource-syntax.yaml"></a>

```
  [DomainName](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-domainname): String
  [HostedZoneArn](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-hostedzonearn): String
  [RecordSetId](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordsetid): String
  [RecordType](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordtype): String
  [TargetResource](#cfn-route53recoveryreadiness-resourceset-dnstargetresource-targetresource): 
    TargetResource
```

## Properties<a name="aws-properties-route53recoveryreadiness-resourceset-dnstargetresource-properties"></a>

`DomainName`  <a name="cfn-route53recoveryreadiness-resourceset-dnstargetresource-domainname"></a>
The domain name that acts as an ingress point to a portion of the customer application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneArn`  <a name="cfn-route53recoveryreadiness-resourceset-dnstargetresource-hostedzonearn"></a>
The hosted zone Amazon Resource Name \(ARN\) that contains the DNS record with the provided name of the target resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordSetId`  <a name="cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordsetid"></a>
The Route 53 record set ID that uniquely identifies a DNS record, given a name and a type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordType`  <a name="cfn-route53recoveryreadiness-resourceset-dnstargetresource-recordtype"></a>
The type of DNS record of the target resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetResource`  <a name="cfn-route53recoveryreadiness-resourceset-dnstargetresource-targetresource"></a>
The target resource that the Route 53 record points to\.  
*Required*: No  
*Type*: [TargetResource](aws-properties-route53recoveryreadiness-resourceset-targetresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)