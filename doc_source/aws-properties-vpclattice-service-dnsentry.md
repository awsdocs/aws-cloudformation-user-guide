# AWS::VpcLattice::Service DnsEntry<a name="aws-properties-vpclattice-service-dnsentry"></a>

Describes the DNS information of a service\.

## Syntax<a name="aws-properties-vpclattice-service-dnsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-service-dnsentry-syntax.json"></a>

```
{
  "[DomainName](#cfn-vpclattice-service-dnsentry-domainname)" : String,
  "[HostedZoneId](#cfn-vpclattice-service-dnsentry-hostedzoneid)" : String
}
```

### YAML<a name="aws-properties-vpclattice-service-dnsentry-syntax.yaml"></a>

```
  [DomainName](#cfn-vpclattice-service-dnsentry-domainname): String
  [HostedZoneId](#cfn-vpclattice-service-dnsentry-hostedzoneid): String
```

## Properties<a name="aws-properties-vpclattice-service-dnsentry-properties"></a>

`DomainName`  <a name="cfn-vpclattice-service-dnsentry-domainname"></a>
The domain name of the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-vpclattice-service-dnsentry-hostedzoneid"></a>
The ID of the hosted zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)