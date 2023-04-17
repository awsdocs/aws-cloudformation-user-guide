# AWS::VpcLattice::ServiceNetworkServiceAssociation DnsEntry<a name="aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry"></a>

DNS information about the service\.

## Syntax<a name="aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry-syntax.json"></a>

```
{
  "[DomainName](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry-domainname)" : String,
  "[HostedZoneId](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry-hostedzoneid)" : String
}
```

### YAML<a name="aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry-syntax.yaml"></a>

```
  [DomainName](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry-domainname): String
  [HostedZoneId](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry-hostedzoneid): String
```

## Properties<a name="aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry-properties"></a>

`DomainName`  <a name="cfn-vpclattice-servicenetworkserviceassociation-dnsentry-domainname"></a>
The domain name of the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-vpclattice-servicenetworkserviceassociation-dnsentry-hostedzoneid"></a>
The ID of the hosted zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)