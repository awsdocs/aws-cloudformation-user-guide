# AWS::Route53::HostedZone<a name="aws-resource-route53-hostedzone"></a>

The `AWS::Route53::HostedZone` resource creates a hosted zone, which can contain a collection of record sets for a domain\. You cannot create a hosted zone for a top\-level domain \(TLD\)\. For more information, see [POST CreateHostedZone](http://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateHostedZone.html) or [POST CreateHostedZone \(Private\)](http://docs.aws.amazon.com/Route53/latest/APIReference/API-create-hosted-zone-private.html) in the *Amazon Route 53 API Reference*\.


+ [Syntax](#aws-resource-route53-hostedzone-syntax)
+ [Properties](#w3ab2c21c10d946b9)
+ [Return Values](#w3ab2c21c10d946c11)
+ [Example](#w3ab2c21c10d946c13)

## Syntax<a name="aws-resource-route53-hostedzone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-hostedzone-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::HostedZone",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-hostedzoneconfig)" : HostedZoneConfig,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-hostedzonetags)" : [  HostedZoneTags, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-queryloggingconfig)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-vpcs)" : [ HostedZoneVPCs, ... ]
  }
}
```

### YAML<a name="aws-resource-route53-hostedzone-syntax.yaml"></a>

```
Type: "AWS::Route53::HostedZone"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-hostedzoneconfig):
    HostedZoneConfig
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-hostedzonetags):
    -  HostedZoneTags
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-queryloggingconfig): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-hostedzone-vpcs):
    - HostedZoneVPCs
```

## Properties<a name="w3ab2c21c10d946b9"></a>

`HostedZoneConfig`  
A complex type that contains an optional comment about your hosted zone\.  
*Required: *No  
*Type*: [Route 53 HostedZoneConfig Property](aws-properties-route53-hostedzone-hostedzoneconfig.md)  
*Update requires*: No interruption

`HostedZoneTags`  
An arbitrary set of tags \(key–value pairs\) for this hosted zone\.  
*Required: *No  
*Type*: List of [Amazon Route 53 HostedZoneTags](aws-properties-route53-hostedzone-hostedzonetags.md)  
*Update requires*: No interruption

`Name`  
The name of the domain\. For resource record types that include a domain name, specify a fully qualified domain name\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`QueryLoggingConfig`  
The configuration for DNS query logging\.  
*Required: *No  
*Type*: [Route 53 QueryLoggingConfig](aws-properties-route53-hostedzone-queryloggingconfig.md)  
*Update requires*: No interruption

`VPCs`  
One or more VPCs that you want to associate with this hosted zone\. When you specify this property, AWS CloudFormation creates a private hosted zone\.  
*Required: *No  
*Type*: List of [Route 53 HostedZoneVPCs](aws-resource-route53-hostedzone-hostedzonevpcs.md)  
If this property was specified previously and you're modifying values, updates require no interruption\. If this property wasn't specified and you add values, updates require replacement\. Also, if this property was specified and you remove all values, updates require replacement\.

## Return Values<a name="w3ab2c21c10d946c11"></a>

### Ref<a name="w3ab2c21c10d946c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myHostedZone" }
```

`Ref` returns the hosted zone ID, such as `Z23ABC4XYZL05B`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d946c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`NameServers`  
Returns the set of name servers for the specific hosted zone\. For example: `ns1.example.com`\.  
This attribute is not supported for private hosted zones\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\. 

## Example<a name="w3ab2c21c10d946c13"></a>

The following template snippet creates a private hosted zone for the `example.com` domain\.

### JSON<a name="aws-resource-route53-hostedzone-example.json"></a>

```
"DNS": {
  "Type": "AWS::Route53::HostedZone",
  "Properties": {
    "HostedZoneConfig": {
      "Comment": "My hosted zone for example.com"
    },
    "Name": "example.com",
    "VPCs": [{
      "VPCId": "vpc-abcd1234",
      "VPCRegion": "ap-northeast-1"
    },
    {
      "VPCId": "vpc-efgh5678",
      "VPCRegion": "us-west-2"
    }],
    "HostedZoneTags" : [{
      "Key": "SampleKey1",
      "Value": "SampleValue1"
    },
    {
      "Key": "SampleKey2",
      "Value": "SampleValue2"
    }]
  }
}
```

### YAML<a name="aws-resource-route53-hostedzone-example.yaml"></a>

```
DNS: 
  Type: "AWS::Route53::HostedZone"
  Properties: 
    HostedZoneConfig: 
      Comment: "My hosted zone for example.com"
    Name: "example.com"
    VPCs: 
      - 
        VPCId: "vpc-abcd1234"
        VPCRegion: "ap-northeast-1"
      - 
        VPCId: "vpc-efgh5678"
        VPCRegion: "us-west-2"
    HostedZoneTags: 
      - 
        Key: "SampleKey1"
        Value: "SampleValue1"
      - 
        Key: "SampleKey2"
        Value: "SampleValue2"
```