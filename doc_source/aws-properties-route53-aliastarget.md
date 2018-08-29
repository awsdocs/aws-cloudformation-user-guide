# Route 53 AliasTarget Property<a name="aws-properties-route53-aliastarget"></a>

`AliasTarget` is a property of the [ AWS::Route53::RecordSet](aws-properties-route53-recordset.md) resource\.

For more information about alias resource record sets, see [Creating Alias Resource Record Sets](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingAliasRRSets.html) in the *Amazon Route 53 Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1643b7"></a>

### JSON<a name="aws-properties-route53-aliastarget-syntax.json"></a>

```
{
  "[DNSName](#cfn-route53-aliastarget-dnshostname)" : String,
  "[EvaluateTargetHealth](#cfn-route53-aliastarget-evaluatetargethealth)" : Boolean,
  "[HostedZoneId](#cfn-route53-aliastarget-hostedzoneid)" : String
}
```

### YAML<a name="aws-properties-route53-aliastarget-syntax.yaml"></a>

```
[DNSName](#cfn-route53-aliastarget-dnshostname): String
[EvaluateTargetHealth](#cfn-route53-aliastarget-evaluatetargethealth): Boolean
[HostedZoneId](#cfn-route53-aliastarget-hostedzoneid): String
```

## Properties<a name="w3ab2c21c14e1643b9"></a>

`DNSName`  <a name="cfn-route53-aliastarget-dnshostname"></a>
The DNS name of the load balancer, the domain name of the CloudFront distribution, the website endpoint of the Amazon S3 bucket, or another record set in the same hosted zone that is the target of the alias\.  
*Type*: String  
*Required*: Yes

`EvaluateTargetHealth`  <a name="cfn-route53-aliastarget-evaluatetargethealth"></a>
Whether Route 53 checks the health of the resource record sets in the alias target when responding to DNS queries\. For more information about using this property, see [EvaluateTargetHealth](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets_Requests.html#change-rrsets-request-evaluate-target-health) in the *Amazon Route 53 API Reference*\.  
*Type*: Boolean  
*Required*: No

`HostedZoneId`  <a name="cfn-route53-aliastarget-hostedzoneid"></a>
The hosted zone ID\. For load balancers, use the canonical hosted zone ID of the load balancer\. For Amazon S3, use the hosted zone ID for your bucket's website endpoint\. For CloudFront, use `Z2FDTNDATAQYW2`\. For a list of hosted zone IDs of other services, see the relevant service in the [AWS Regions and Endpoints](http://docs.aws.amazon.com/general/latest/gr/rande.html)\.  
*Type*: String  
*Required*: Yes