# Route 53 template snippets<a name="quickref-route53"></a>

**Topics**
+ [Amazon Route 53 resource record set using hosted zone name or ID](#scenario-route53-recordset-by-host)
+ [Using RecordSetGroup to set up weighted resource record sets](#scenario-recordsetgroup-weighted)
+ [Using RecordSetGroup to set up an alias resource record set](#scenario-recordsetgroup-zoneapex)
+ [Alias resource record set for a CloudFront distribution](#w7739ab1c27c22c81c11)

## Amazon Route 53 resource record set using hosted zone name or ID<a name="scenario-route53-recordset-by-host"></a>

When you create an Amazon Route 53 resource record set, you must specify the hosted zone where you want to add it\. AWS CloudFormation provides two ways to specify a hosted zone:
+ You can explicitly specify the hosted zone using the `HostedZoneId` property\. 
+ You can have AWS CloudFormation find the hosted zone using the `HostedZoneName` property\. If you use the `HostedZoneName` property and there are multiple hosted zones with the same name, AWS CloudFormation doesn't create the stack\.

### Adding RecordSet using HostedZoneId<a name="scenario-recordset-using-id"></a>

This example adds an Amazon Route 53 resource record set containing an SPF record for the domain name `mysite.example.com` that uses the `HostedZoneId` property to specify the hosted zone\.

#### JSON<a name="quickref-route53-example-1.json"></a>

```
 1. "myDNSRecord" : {
 2.   "Type" : "AWS::Route53::RecordSet",
 3.   "Properties" : 
 4.   {
 5.     "HostedZoneId" : "Z3DG6IL3SJCGPX",
 6.     "Name" : "mysite.example.com.",
 7.     "Type" : "SPF",
 8.     "TTL" : "900",
 9.     "ResourceRecords" : [ "\"v=spf1 ip4:192.168.0.1/16 -all\"" ]
10.   }
11. }
```

#### YAML<a name="quickref-route53-example-1.yaml"></a>

```
1. myDNSRecord:
2.   Type: AWS::Route53::RecordSet
3.   Properties:
4.     HostedZoneId: Z3DG6IL3SJCGPX
5.     Name: mysite.example.com.
6.     Type: SPF
7.     TTL: '900'
8.     ResourceRecords:
9.     - '"v=spf1 ip4:192.168.0.1/16 -all"'
```

### Adding RecordSet using HostedZoneName<a name="scenario-recordset-using-name"></a>

This example adds an Amazon Route 53 resource record set for the domain name "mysite\.example\.com" using the `HostedZoneName` property to specify the hosted zone\.

#### JSON<a name="quickref-route53-example-2.json"></a>

```
 1. "myDNSRecord2" : {
 2.             "Type" : "AWS::Route53::RecordSet",
 3.             "Properties" : {
 4.                 "HostedZoneName" : "example.com.",
 5.                 "Name" : "mysite.example.com.",
 6.                 "Type" : "A",
 7.                 "TTL" : "900",
 8.                 "ResourceRecords" : [
 9.                     "192.168.0.1",
10.                     "192.168.0.2"
11.                 ]
12.             }
13.         }
```

#### YAML<a name="quickref-route53-example-2.yaml"></a>

```
 1. myDNSRecord2:
 2.   Type: AWS::Route53::RecordSet
 3.   Properties:
 4.     HostedZoneName: example.com.
 5.     Name: mysite.example.com.
 6.     Type: A
 7.     TTL: '900'
 8.     ResourceRecords:
 9.     - 192.168.0.1
10.     - 192.168.0.2
```

## Using RecordSetGroup to set up weighted resource record sets<a name="scenario-recordsetgroup-weighted"></a>

This example uses an [AWS::Route53::RecordSetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-recordsetgroup.html) to set up two CNAME records for the "example\.com\." hosted zone\. The `RecordSets` property contains the CNAME record sets for the "mysite\.example\.com" DNS name\. Each record set contains an identifier \(`SetIdentifier`\) and weight \(`Weight`\)\. The proportion of internet traffic that is routed to the resources is based on the following calculations:
+ `Frontend One`: `140/(140+60)` = `140/200` = 70%
+ `Frontend Two`: `60/(140+60)` = `60/200` = 30%

For more information about weighted resource record sets, see [Weighted routing](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-weighted) in the *Amazon Route 53 Developer Guide*\.

### JSON<a name="quickref-route53-example-3.json"></a>

```
 1.         "myDNSOne" : {
 2.             "Type" : "AWS::Route53::RecordSetGroup",
 3.             "Properties" : {
 4.                 "HostedZoneName" : "example.com.",
 5.                 "Comment" : "Weighted RR for my frontends.",
 6.                 "RecordSets" : [
 7.                   {
 8.                     "Name" : "mysite.example.com.",
 9.                     "Type" : "CNAME",
10.                     "TTL" : "900",
11.                     "SetIdentifier" : "Frontend One",
12.                     "Weight" : "140",
13.                     "ResourceRecords" : ["example-ec2.amazonaws.com"]
14.                   },
15.                   {
16.                     "Name" : "mysite.example.com.",
17.                     "Type" : "CNAME",
18.                     "TTL" : "900",
19.                     "SetIdentifier" : "Frontend Two",
20.                     "Weight" : "60",
21.                     "ResourceRecords" : ["example-ec2-larger.amazonaws.com"]
22.                   }
23.                   ]
24.             }
25.         }
```

### YAML<a name="quickref-route53-example-3.yaml"></a>

```
 1. myDNSOne:
 2.   Type: AWS::Route53::RecordSetGroup
 3.   Properties:
 4.     HostedZoneName: example.com.
 5.     Comment: Weighted RR for my frontends.
 6.     RecordSets:
 7.     - Name: mysite.example.com.
 8.       Type: CNAME
 9.       TTL: '900'
10.       SetIdentifier: Frontend One
11.       Weight: '4'
12.       ResourceRecords:
13.       - example-ec2.amazonaws.com
14.     - Name: mysite.example.com.
15.       Type: CNAME
16.       TTL: '900'
17.       SetIdentifier: Frontend Two
18.       Weight: '6'
19.       ResourceRecords:
20.       - example-ec2-larger.amazonaws.com
```

## Using RecordSetGroup to set up an alias resource record set<a name="scenario-recordsetgroup-zoneapex"></a>

The following examples use an [AWS::Route53::RecordSetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-recordsetgroup.html) to set up an alias resource record set named `example.com` that routes traffic to an ELB Version 1 \(Classic\) load balancer and a Version 2 \(Application or Network\) load balancer\. The [AliasTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-aliastarget.html) property specifies the hosted zone ID and DNS name for the myELB LoadBalancer by using the [GetAtt](intrinsic-function-reference-getatt.md) intrinsic function\. `GetAtt` retrieves different properties of myELB resource, depending on whether you're routing traffic to a Version 1 or Version 2 load balancer:
+ Version 1 load balancer: `CanonicalHostedZoneNameID` and `DNSName`
+ Version 2 load balancer: `CanonicalHostedZoneID` and `DNSName`

For more information about alias resource record sets, see [Choosing between alias and non\-alias records](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html) in the *Route 53 Developer Guide*\.

### JSON for version 1 load balancer<a name="quickref-route53-example-4.json"></a>

```
 1.       "myELB" : {
 2.         "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
 3.         "Properties" : {
 4.             "AvailabilityZones" : [ "us-east-1a" ],
 5.             "Listeners" : [ {
 6.                 "LoadBalancerPort" : "80",
 7.                 "InstancePort" : "80",
 8.                 "Protocol" : "HTTP"
 9.             } ]
10.         }
11.       },
12.       "myDNS" : {
13.         "Type" : "AWS::Route53::RecordSetGroup",
14.         "Properties" : {
15.           "HostedZoneName" : "example.com.",
16.           "Comment" : "Zone apex alias targeted to myELB LoadBalancer.",
17.           "RecordSets" : [
18.             {
19.               "Name" : "example.com.",
20.               "Type" : "A",
21.               "AliasTarget" : {
22.                   "HostedZoneId" : { "Fn::GetAtt" : ["myELB", "CanonicalHostedZoneNameID"] },
23.                   "DNSName" : { "Fn::GetAtt" : ["myELB","DNSName"] }
24.               }
25.             }
26.           ]
27.         }
28.     }
```

### YAML for version 1 load balancer<a name="quickref-route53-example-4.yaml"></a>

```
 1. myELB:
 2.   Type: AWS::ElasticLoadBalancing::LoadBalancer
 3.   Properties:
 4.     AvailabilityZones:
 5.     - "us-east-1a"
 6.     Listeners:
 7.     - LoadBalancerPort: '80'
 8.       InstancePort: '80'
 9.       Protocol: HTTP
10. myDNS:
11.   Type: AWS::Route53::RecordSetGroup
12.   Properties:
13.     HostedZoneName: example.com.
14.     Comment: Zone apex alias targeted to myELB LoadBalancer.
15.     RecordSets:
16.     - Name: example.com.
17.       Type: A
18.       AliasTarget:
19.         HostedZoneId: !GetAtt 'myELB.CanonicalHostedZoneNameID'
20.         DNSName: !GetAtt 'myELB.DNSName'
```

### JSON for version 2 load balancer<a name="quickref-route53-example-4-v2.json"></a>

```
 1.       "myELB" : {
 2.         "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
 3.         "Properties" : {
 4.             "Subnets" : [ 
 5.                 {"Ref": "SubnetAZ1"}, 
 6.                 {"Ref" : "SubnetAZ2"}
 7.             ]
 8.         }
 9.       },
10.       "myDNS" : {
11.         "Type" : "AWS::Route53::RecordSetGroup",
12.         "Properties" : {
13.           "HostedZoneName" : "example.com.",
14.           "Comment" : "Zone apex alias targeted to myELB LoadBalancer.",
15.           "RecordSets" : [
16.             {
17.               "Name" : "example.com.",
18.               "Type" : "A",
19.               "AliasTarget" : {
20.                   "HostedZoneId" : { "Fn::GetAtt" : ["myELB", "CanonicalHostedZoneID"] },
21.                   "DNSName" : { "Fn::GetAtt" : ["myELB","DNSName"] }
22.               }
23.             }
24.           ]
25.         }
26.     }
```

### YAML for version 2 load balancer<a name="quickref-route53-example-4-v2.yaml"></a>

```
 1. myELB:
 2.   Type: AWS::ElasticLoadBalancingV2::LoadBalancer
 3.   Properties:
 4.     Subnets:
 5.     - Ref: SubnetAZ1
 6.     - Ref: SubnetAZ2
 7. myDNS:
 8.   Type: AWS::Route53::RecordSetGroup
 9.   Properties:
10.     HostedZoneName: example.com.
11.     Comment: Zone apex alias targeted to myELB LoadBalancer.
12.     RecordSets:
13.     - Name: example.com.
14.       Type: A
15.       AliasTarget:
16.         HostedZoneId: !GetAtt 'myELB.CanonicalHostedZoneID'
17.         DNSName: !GetAtt 'myELB.DNSName'
```

## Alias resource record set for a CloudFront distribution<a name="w7739ab1c27c22c81c11"></a>

The following example creates an alias record set that routes queries to the specified CloudFront distribution\.

**Note**  
When you create alias resource record sets, you must specify `Z2FDTNDATAQYW2` for the `HostedZoneId` property, as shown in the following example\. Alias resource record sets for CloudFront can't be created in a private zone\.

### JSON<a name="quickref-route53-example-5.json"></a>

```
 1. {
 2.     "myDNS": {
 3.         "Type": "AWS::Route53::RecordSetGroup",
 4.         "Properties": {
 5.             "HostedZoneId": {
 6.                 "Ref": "myHostedZoneID"
 7.             },
 8.             "RecordSets": [
 9.                 {
10.                     "Name": {
11.                         "Ref": "myRecordSetDomainName"
12.                     },
13.                     "Type": "A",
14.                     "AliasTarget": {
15.                         "HostedZoneId": "Z2FDTNDATAQYW2",
16.                         "DNSName": {
17.                             "Fn::GetAtt": [
18.                                 "myCloudFrontDistribution",
19.                                 "DomainName"
20.                             ]
21.                         }
22.                     }
23.                 }
24.             ]
25.         }
26.     }
27. }
```

### YAML<a name="quickref-route53-example-5.yaml"></a>

```
 1. myDNS:
 2.   Type: 'AWS::Route53::RecordSetGroup'
 3.   Properties:
 4.     HostedZoneId: !Ref myHostedZoneID
 5.     RecordSets:
 6.       - Name: !Ref myRecordSetDomainName
 7.         Type: A
 8.         AliasTarget:
 9.           HostedZoneId: Z2FDTNDATAQYW2
10.           DNSName: !GetAtt 
11.             - myCloudFrontDistribution
12.             - DomainName
```