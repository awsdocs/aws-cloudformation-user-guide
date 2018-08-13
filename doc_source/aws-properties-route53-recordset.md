# AWS::Route53::RecordSet<a name="aws-properties-route53-recordset"></a>

The `AWS::Route53::RecordSet` type can be used as a standalone resource or as an embedded property in the [AWS::Route53::RecordSetGroup](aws-properties-route53-recordsetgroup.md) type\. Note that some `AWS::Route53::RecordSet` properties are valid only when used within `AWS::Route53::RecordSetGroup`\.

For more information about constraints and values for each property, see [POST CreateHostedZone](http://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateHostedZone.html) for hosted zones and [POST ChangeResourceRecordSet](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html) for resource record sets\.

**Topics**
+ [Syntax](#aws-resource-route53-recordset-syntax)
+ [Properties](#w3ab2c21c10e1023c11)
+ [Return Value](#w3ab2c21c10e1023c13)
+ [Example](#w3ab2c21c10e1023c15)

## Syntax<a name="aws-resource-route53-recordset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-recordset-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::RecordSet",
  "Properties" : {
    "[AliasTarget](#cfn-route53-recordset-aliastarget)" : [*AliasTarget*](aws-properties-route53-aliastarget.md),
    "[Comment](#cfn-route53-recordset-comment)" : String,
    "[Failover](#cfn-route53-recordset-failover)" : String,
    "[GeoLocation](#cfn-route53-recordset-geolocation)" : GeoLocation,
    "[HealthCheckId](#cfn-route53-recordset-healthcheckid)" : String,
    "[HostedZoneId](#cfn-route53-recordset-hostedzoneid)" : String,
    "[HostedZoneName](#cfn-route53-recordset-hostedzonename)" : String,
    "[Name](#cfn-route53-recordset-name)" : String,
    "[Region](#cfn-route53-recordset-region)" : String,
    "[ResourceRecords](#cfn-route53-recordset-resourcerecords)" : [ String ],
    "[SetIdentifier](#cfn-route53-recordset-setidentifier)" : String,
    "[TTL](#cfn-route53-recordset-ttl)" : String,
    "[Type](#cfn-route53-recordset-type)" : String,
    "[Weight](#cfn-route53-recordset-weight)" : Integer
  }
}
```

### YAML<a name="aws-resource-route53-recordset-syntax.yaml"></a>

```
Type: "AWS::Route53::RecordSet"
Properties: 
  [AliasTarget](#cfn-route53-recordset-aliastarget): 
    [*AliasTarget*](aws-properties-route53-aliastarget.md)
  [Comment](#cfn-route53-recordset-comment): String
  [Failover](#cfn-route53-recordset-failover): String
  [GeoLocation](#cfn-route53-recordset-geolocation):
    GeoLocation
  [HealthCheckId](#cfn-route53-recordset-healthcheckid): String
  [HostedZoneId](#cfn-route53-recordset-hostedzoneid): String
  [HostedZoneName](#cfn-route53-recordset-hostedzonename): String
  [Name](#cfn-route53-recordset-name): String
  [Region](#cfn-route53-recordset-region): String
  [ResourceRecords](#cfn-route53-recordset-resourcerecords):
    - String
  [SetIdentifier](#cfn-route53-recordset-setidentifier): String
  [TTL](#cfn-route53-recordset-ttl): String
  [Type](#cfn-route53-recordset-type): String
  [Weight](#cfn-route53-recordset-weight): Integer
```

## Properties<a name="w3ab2c21c10e1023c11"></a>

`AliasTarget`  <a name="cfn-route53-recordset-aliastarget"></a>
*Alias resource record sets only:* Information about the domain to which you are redirecting traffic\.  
If you specify this property, do not specify the `TTL` property\. The alias uses a TTL value from the alias target record\.  
For more information about alias resource record sets, see [Creating Alias Resource Record Sets](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingAliasRRSets.html) in the *Route 53 Developer Guide* and [POST ChangeResourceRecordSets](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html#API_ChangeResourceRecordSets_RequestAliasSyntax) in the Route 53 API reference\.  
*Required*: Conditional\. Required if you are creating an alias resource record set\.   
*Type*: [AliasTarget](aws-properties-route53-aliastarget.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Comment`  <a name="cfn-route53-recordset-comment"></a>
Any comments that you want to include about the hosted zone\.  
If the record set is part of a record set group, this property isn't valid\. Don't specify this property\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Failover`  <a name="cfn-route53-recordset-failover"></a>
Designates the record set as a `PRIMARY` or `SECONDARY` failover record set\. When you have more than one resource performing the same function, you can configure Route 53 to check the health of your resources and use only health resources to respond to DNS queries\. You cannot create nonfailover resource record sets that have the same `Name` and `Type` property values as failover resource record sets\. For more information, see the [Failover](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ResourceRecordSet.html#Route53-Type-ResourceRecordSet-Failover) content in the *Amazon Route 53 API Reference*\.  
If you specify this property, you must specify the `SetIdentifier` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GeoLocation`  <a name="cfn-route53-recordset-geolocation"></a>
Describes how Route 53 responds to DNS queries based on the geographic origin of the query\. This property is not compatible with the `Region` property\.  
*Required*: No  
*Type*: [Route 53 Record Set GeoLocation Property](aws-properties-route53-recordset-geolocation.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckId`  <a name="cfn-route53-recordset-healthcheckid"></a>
The health check ID that you want to apply to this record set\. Route 53 returns this resource record set in response to a DNS query only while record set is healthy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HostedZoneId`  <a name="cfn-route53-recordset-hostedzoneid"></a>
The ID of the hosted zone\.  
*Required*: Conditional\. You must specify either the `HostedZoneName` or `HostedZoneId`, but you cannot specify both\. If this record set is part of a record set group, do not specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`HostedZoneName`  <a name="cfn-route53-recordset-hostedzonename"></a>
The name of the domain for the hosted zone where you want to add the record set\.  
When you create a stack using an `AWS::Route53::RecordSet` that specifies `HostedZoneName`, AWS CloudFormation attempts to find a hosted zone whose name matches the `HostedZoneName`\. If AWS CloudFormation cannot find a hosted zone with a matching domain name, or if there is more than one hosted zone with the specified domain name, AWS CloudFormation will not create the stack\.  
If you have multiple hosted zones with the same domain name, you must explicitly specify the hosted zone using `HostedZoneId`\.  
*Required*: Conditional\. You must specify either the `HostedZoneName` or `HostedZoneId`, but you cannot specify both\. If this record set is part of a record set group, do not specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-route53-recordset-name"></a>
The name of the domain\. You must specify a fully qualified domain name that ends with a period as the last label indication\. If you omit the final period, Route 53 adds it\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Region`  <a name="cfn-route53-recordset-region"></a>
Latency resource record sets only: The Amazon EC2 region where the resource that is specified in this resource record set resides\. The resource typically is an AWS resource, for example, Amazon EC2 instance or an Elastic Load Balancing load balancer, and is referred to by an IP address or a DNS domain name, depending on the record type\.  
When Route 53 receives a DNS query for a domain name and type for which you have created latency resource record sets, Route 53 selects the latency resource record set that has the lowest latency between the end user and the associated Amazon EC2 region\. Route 53 then returns the value that is associated with the selected resource record set\.  
The following restrictions must be followed:  
+ You can only specify one resource record per latency resource record set\.
+ You can only create one latency resource record set for each Amazon EC2 region\.
+ You are not required to create latency resource record sets for all Amazon EC2 regions\. Route 53 will choose the region with the best latency from among the regions for which you create latency resource record sets\.
+ You cannot create both weighted and latency resource record sets that have the same values for the Name and Type elements\.
+ This property is not compatible with the `GeoLocation` property\.
To see a list of regions by service, see [Regions and Endpoints](http://docs.aws.amazon.com/general/latest/gr/rande.html) in the *AWS General Reference*\.

`ResourceRecords`  <a name="cfn-route53-recordset-resourcerecords"></a>
List of resource records to add\. Each record should be in the format appropriate for the record type specified by the `Type` property\. For information about different record types and their record formats, see [Values for Basic Resource Record Sets](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-values-basic.html) and [Appendix: Domain Name Format](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DomainNameFormat.html) in the *Route 53 Developer Guide*\.  
 *Required*: Conditional\. If you don't specify the `AliasTarget` property, you must specify this property\. If you are creating an alias resource record set, do not specify this property\.  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SetIdentifier`  <a name="cfn-route53-recordset-setidentifier"></a>
A unique identifier that differentiates among multiple resource record sets that have the same combination of DNS name and type\.  
*Required*: Conditional\. Required if you are creating a weighted, latency, failover, or geolocation resource record set\.  
For more information, see the [SetIdentifier](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ResourceRecordSet.html#Route53-Type-ResourceRecordSet-SetIdentifier) content in the *Route 53 Developer Guide*\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TTL`  <a name="cfn-route53-recordset-ttl"></a>
The resource record cache time to live \(TTL\), in seconds\. If you specify this property, do not specify the `AliasTarget` property\. For alias target records, the alias uses a TTL value from the target\.  
If you specify this property, you must specify the `ResourceRecords` property\.  
*Required*: Conditional\. If you don't specify the `AliasTarget` property, you must specify this property\. If you are creating an alias resource record set, do not specify this property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-route53-recordset-type"></a>
The type of records to add\. For valid values, see the [Type](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ResourceRecordSet.html#Route53-Type-ResourceRecordSet-Type) content in the *Amazon Route 53 API Reference*\.  
In AWS CloudFormation, you cannot modify the NS and SOA records for a hosted zone created automatically by Route 53\. Specifically, you can't create or delete NS or SOA records for the root domain of your hosted zone, but you can create them for subdomains to delegate\. For example, for hosted zone `mydomain.net`, you cannot create an NS record for `mydomain.net` but you can create an NS record for `nnnn.mydomain.net` for delegation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Weight`  <a name="cfn-route53-recordset-weight"></a>
*Weighted resource record sets only:* Among resource record sets that have the same combination of DNS name and type, a value that determines what portion of traffic for the current resource record set is routed to the associated location\.  
For more information about weighted resource record sets, see [Setting Up Weighted Resource Record Sets](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/WeightedResourceRecordSets.html) in the *Route 53 Developer Guide*\.  
*Required*: Conditional\. Required if you are creating a weighted resource record set\.  
*Type*: Number\. Weight expects integer values\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1023c13"></a>

When you specify an `AWS::Route53::RecordSet` type as an argument to the `Ref` function, AWS CloudFormation returns the value of the domain name of the record set\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10e1023c15"></a>

### Mapping an Route 53 A record to the public IP of an Amazon EC2 instance<a name="w3ab2c21c10e1023c15b2"></a>

#### JSON<a name="aws-resource-route53-recordset-example.json"></a>

```
"Resources" : {
   "Ec2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
         "ImageId" : { "Fn::FindInMap" : [
            "RegionMap", { "Ref" : "AWS::Region" }, "AMI"
         ] }
      }
   },
   "myDNSRecord" : {
      "Type" : "AWS::Route53::RecordSet",
      "Properties" : {
         "HostedZoneName" : { "Ref" : "HostedZoneResource" },
         "Comment" : "DNS name for my instance.",  
         "Name" : {
            "Fn::Join" : [ "", [
               {"Ref" : "Ec2Instance"}, ".",
               {"Ref" : "AWS::Region"}, ".",
               {"Ref" : "HostedZone"} ,"."
            ] ]
         },
         "Type" : "A",
         "TTL" : "900",
         "ResourceRecords" : [
            { "Fn::GetAtt" : [ "Ec2Instance", "PublicIp" ] }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-route53-recordset-example.yaml"></a>

```
Resources:
  Ec2Instance:
    Type: AWS::EC2::Instance
    Properties:
      ImageId: !FindInMap [RegionMap, !Ref 'AWS::Region', AMI]
  myDNSRecord:
    Type: AWS::Route53::RecordSet
    Properties:
      HostedZoneName: !Ref 'HostedZoneResource'
      Comment: DNS name for my instance.
      Name: !Join ['', [!Ref 'Ec2Instance', ., !Ref 'AWS::Region', ., !Ref 'HostedZone', .]]
      Type: A
      TTL: '900'
      ResourceRecords:
      - !GetAtt Ec2Instance.PublicIp
```

### Additional Information<a name="w3ab2c21c10e1023c15b4"></a>

For additional `AWS::Route53::RecordSet` snippets, see [Route 53 Template Snippets](quickref-route53.md) \.