# AWS::Route53::RecordSetGroup RecordSet<a name="aws-properties-route53-recordset-1"></a>

Information about one record that you want to create\.

## Syntax<a name="aws-properties-route53-recordset-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-recordset-1-syntax.json"></a>

```
{
  "[AliasTarget](#cfn-route53-recordset-aliastarget)" : AliasTarget,
  "[Comment](#cfn-route53-recordset-comment)" : String,
  "[Failover](#cfn-route53-recordset-failover)" : String,
  "[GeoLocation](#cfn-route53-recordset-geolocation)" : GeoLocation,
  "[HealthCheckId](#cfn-route53-recordset-healthcheckid)" : String,
  "[HostedZoneId](#cfn-route53-recordset-hostedzoneid)" : String,
  "[HostedZoneName](#cfn-route53-recordset-hostedzonename)" : String,
  "[MultiValueAnswer](#cfn-route53-recordset-multivalueanswer)" : Boolean,
  "[Name](#cfn-route53-recordset-name)" : String,
  "[Region](#cfn-route53-recordset-region)" : String,
  "[ResourceRecords](#cfn-route53-recordset-resourcerecords)" : [ String, ... ],
  "[SetIdentifier](#cfn-route53-recordset-setidentifier)" : String,
  "[TTL](#cfn-route53-recordset-ttl)" : String,
  "[Type](#cfn-route53-recordset-type)" : String,
  "[Weight](#cfn-route53-recordset-weight)" : Integer
}
```

### YAML<a name="aws-properties-route53-recordset-1-syntax.yaml"></a>

```
  [AliasTarget](#cfn-route53-recordset-aliastarget): 
    AliasTarget
  [Comment](#cfn-route53-recordset-comment): String
  [Failover](#cfn-route53-recordset-failover): String
  [GeoLocation](#cfn-route53-recordset-geolocation): 
    GeoLocation
  [HealthCheckId](#cfn-route53-recordset-healthcheckid): String
  [HostedZoneId](#cfn-route53-recordset-hostedzoneid): String
  [HostedZoneName](#cfn-route53-recordset-hostedzonename): String
  [MultiValueAnswer](#cfn-route53-recordset-multivalueanswer): Boolean
  [Name](#cfn-route53-recordset-name): String
  [Region](#cfn-route53-recordset-region): String
  [ResourceRecords](#cfn-route53-recordset-resourcerecords): 
    - String
  [SetIdentifier](#cfn-route53-recordset-setidentifier): String
  [TTL](#cfn-route53-recordset-ttl): String
  [Type](#cfn-route53-recordset-type): String
  [Weight](#cfn-route53-recordset-weight): Integer
```

## Properties<a name="aws-properties-route53-recordset-1-properties"></a>

`AliasTarget`  <a name="cfn-route53-recordset-aliastarget"></a>
 *Alias resource record sets only:* Information about the AWS resource, such as a CloudFront distribution or an Amazon S3 bucket, that you want to route traffic to\.   
If you're creating resource records sets for a private hosted zone, note the following:  
+ You can't create an alias resource record set in a private hosted zone to route traffic to a CloudFront distribution\.
+ Creating geolocation alias resource record sets or latency alias resource record sets in a private hosted zone is unsupported\.
+ For information about creating failover resource record sets in a private hosted zone, see [Configuring Failover in a Private Hosted Zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-private-hosted-zones.html) in the *Amazon Route 53 Developer Guide*\.
*Required*: No  
*Type*: [AliasTarget](aws-properties-route53-aliastarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-route53-recordset-comment"></a>
 *Optional:* Any comments you want to include about a change batch request\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Failover`  <a name="cfn-route53-recordset-failover"></a>
 *Failover resource record sets only:* To configure failover, you add the `Failover` element to two resource record sets\. For one resource record set, you specify `PRIMARY` as the value for `Failover`; for the other resource record set, you specify `SECONDARY`\. In addition, you include the `HealthCheckId` element and specify the health check that you want Amazon Route 53 to perform for each resource record set\.  
Except where noted, the following failover behaviors assume that you have included the `HealthCheckId` element in both resource record sets:  
+ When the primary resource record set is healthy, Route 53 responds to DNS queries with the applicable value from the primary resource record set regardless of the health of the secondary resource record set\.
+ When the primary resource record set is unhealthy and the secondary resource record set is healthy, Route 53 responds to DNS queries with the applicable value from the secondary resource record set\.
+ When the secondary resource record set is unhealthy, Route 53 responds to DNS queries with the applicable value from the primary resource record set regardless of the health of the primary resource record set\.
+ If you omit the `HealthCheckId` element for the secondary resource record set, and if the primary resource record set is unhealthy, Route 53 always responds to DNS queries with the applicable value from the secondary resource record set\. This is true regardless of the health of the associated endpoint\.
You can't create non\-failover resource record sets that have the same values for the `Name` and `Type` elements as failover resource record sets\.  
For failover alias resource record sets, you must also include the `EvaluateTargetHealth` element and set the value to true\.  
For more information about configuring failover for Route 53, see the following topics in the *Amazon Route 53 Developer Guide*:   
+  [Route 53 Health Checks and DNS Failover](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html) 
+  [Configuring Failover in a Private Hosted Zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-private-hosted-zones.html) 
*Required*: No  
*Type*: String  
*Allowed values*: `PRIMARY | SECONDARY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoLocation`  <a name="cfn-route53-recordset-geolocation"></a>
 *Geolocation resource record sets only:* A complex type that lets you control how Amazon Route 53 responds to DNS queries based on the geographic origin of the query\. For example, if you want all queries from Africa to be routed to a web server with an IP address of `192.0.2.111`, create a resource record set with a `Type` of `A` and a `ContinentCode` of `AF`\.  
Although creating geolocation and geolocation alias resource record sets in a private hosted zone is allowed, it's not supported\.
If you create separate resource record sets for overlapping geographic regions \(for example, one resource record set for a continent and one for a country on the same continent\), priority goes to the smallest geographic region\. This allows you to route most queries for a continent to one resource and to route queries for a country on that continent to a different resource\.  
You can't create two geolocation resource record sets that specify the same geographic location\.  
The value `*` in the `CountryCode` element matches all geographic locations that aren't specified in other geolocation resource record sets that have the same values for the `Name` and `Type` elements\.  
Geolocation works by mapping IP addresses to locations\. However, some IP addresses aren't mapped to geographic locations, so even if you create geolocation resource record sets that cover all seven continents, Route 53 will receive some DNS queries from locations that it can't identify\. We recommend that you create a resource record set for which the value of `CountryCode` is `*`\. Two groups of queries are routed to the resource that you specify in this record: queries that come from locations for which you haven't created geolocation resource record sets and queries from IP addresses that aren't mapped to a location\. If you don't create a `*` resource record set, Route 53 returns a "no answer" response for queries from those locations\.
You can't create non\-geolocation resource record sets that have the same values for the `Name` and `Type` elements as geolocation resource record sets\.  
*Required*: No  
*Type*: [GeoLocation](aws-properties-route53-recordset-geolocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckId`  <a name="cfn-route53-recordset-healthcheckid"></a>
If you want Amazon Route 53 to return this resource record set in response to a DNS query only when the status of a health check is healthy, include the `HealthCheckId` element and specify the ID of the applicable health check\.  
Route 53 determines whether a resource record set is healthy based on one of the following:  
+ By periodically sending a request to the endpoint that is specified in the health check
+ By aggregating the status of a specified group of health checks \(calculated health checks\)
+ By determining the current state of a CloudWatch alarm \(CloudWatch metric health checks\)
Route 53 doesn't check the health of the endpoint that is specified in the resource record set, for example, the endpoint specified by the IP address in the `Value` element\. When you add a `HealthCheckId` element to a resource record set, Route 53 checks the health of the endpoint that you specified in the health check\. 
For more information, see the following topics in the *Amazon Route 53 Developer Guide*:  
+  [How Amazon Route 53 Determines Whether an Endpoint Is Healthy](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-determining-health-of-endpoints.html) 
+  [Route 53 Health Checks and DNS Failover](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html) 
+  [Configuring Failover in a Private Hosted Zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-private-hosted-zones.html) 
 **When to Specify HealthCheckId**   
Specifying a value for `HealthCheckId` is useful only when Route 53 is choosing between two or more resource record sets to respond to a DNS query, and you want Route 53 to base the choice in part on the status of a health check\. Configuring health checks makes sense only in the following configurations:  
+  **Non\-alias resource record sets**: You're checking the health of a group of non\-alias resource record sets that have the same routing policy, name, and type \(such as multiple weighted records named www\.example\.com with a type of A\) and you specify health check IDs for all the resource record sets\. 

  If the health check status for a resource record set is healthy, Route 53 includes the record among the records that it responds to DNS queries with\.

  If the health check status for a resource record set is unhealthy, Route 53 stops responding to DNS queries using the value for that resource record set\.

  If the health check status for all resource record sets in the group is unhealthy, Route 53 considers all resource record sets in the group healthy and responds to DNS queries accordingly\. 
+  **Alias resource record sets**: You specify the following settings:
  + You set `EvaluateTargetHealth` to true for an alias resource record set in a group of resource record sets that have the same routing policy, name, and type \(such as multiple weighted records named www\.example\.com with a type of A\)\. 
  + You configure the alias resource record set to route traffic to a non\-alias resource record set in the same hosted zone\.
  + You specify a health check ID for the non\-alias resource record set\. 

  If the health check status is healthy, Route 53 considers the alias resource record set to be healthy and includes the alias record among the records that it responds to DNS queries with\.

  If the health check status is unhealthy, Route 53 stops responding to DNS queries using the alias resource record set\.
**Note**  
The alias resource record set can also route traffic to a *group* of non\-alias resource record sets that have the same routing policy, name, and type\. In that configuration, associate health checks with all of the resource record sets in the group of non\-alias resource record sets\.
 **Geolocation Routing**   
For geolocation resource record sets, if an endpoint is unhealthy, Route 53 looks for a resource record set for the larger, associated geographic region\. For example, suppose you have resource record sets for a state in the United States, for the entire United States, for North America, and a resource record set that has `*` for `CountryCode` is `*`, which applies to all locations\. If the endpoint for the state resource record set is unhealthy, Route 53 checks for healthy resource record sets in the following order until it finds a resource record set for which the endpoint is healthy:  
+ The United States
+ North America
+ The default resource record set
 **Specifying the Health Check Endpoint by Domain Name**   
If your health checks specify the endpoint only by domain name, we recommend that you create a separate health check for each endpoint\. For example, create a health check for each `HTTP` server that is serving content for `www.example.com`\. For the value of `FullyQualifiedDomainName`, specify the domain name of the server \(such as `us-east-2-www.example.com`\), not the name of the resource record sets \(`www.example.com`\)\.  
Health check results will be unpredictable if you do the following:  
+ Create a health check that has the same value for `FullyQualifiedDomainName` as the name of a resource record set\.
+ Associate that health check with the resource record set\.
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-route53-recordset-hostedzoneid"></a>
The ID of the hosted zone that you want to create records in\.  
Specify either `HostedZoneName` or `HostedZoneId`, but not both\. If you have multiple hosted zones with the same domain name, you must specify the hosted zone using `HostedZoneId`\.   
*Required*: No  
*Type*: String  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneName`  <a name="cfn-route53-recordset-hostedzonename"></a>
The name of the hosted zone that you want to create records in\.  
When you create a stack using an `AWS::Route53::RecordSet` that specifies `HostedZoneName`, AWS CloudFormation attempts to find a hosted zone whose name matches the `HostedZoneName`\. If AWS CloudFormation can't find a hosted zone with a matching domain name, or if there is more than one hosted zone with the specified domain name, AWS CloudFormation will not create the stack\.   
Specify either `HostedZoneName` or `HostedZoneId`, but not both\. If you have multiple hosted zones with the same domain name, you must specify the hosted zone using `HostedZoneId`\.   
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiValueAnswer`  <a name="cfn-route53-recordset-multivalueanswer"></a>
 *Multivalue answer resource record sets only*: To route traffic approximately randomly to multiple resources, such as web servers, create one multivalue answer record for each resource and specify `true` for `MultiValueAnswer`\. Note the following:  
+ If you associate a health check with a multivalue answer resource record set, Amazon Route 53 responds to DNS queries with the corresponding IP address only when the health check is healthy\.
+ If you don't associate a health check with a multivalue answer record, Route 53 always considers the record to be healthy\.
+ Route 53 responds to DNS queries with up to eight healthy records; if you have eight or fewer healthy records, Route 53 responds to all DNS queries with all the healthy records\.
+ If you have more than eight healthy records, Route 53 responds to different DNS resolvers with different combinations of healthy records\.
+ When all records are unhealthy, Route 53 responds to DNS queries with up to eight unhealthy records\.
+ If a resource becomes unavailable after a resolver caches a response, client software typically tries another of the IP addresses in the response\.
You can't create multivalue answer alias records\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53-recordset-name"></a>
For `ChangeResourceRecordSets` requests, the name of the record that you want to create, update, or delete\. For `ListResourceRecordSets` responses, the name of a record in the specified hosted zone\.  
 **ChangeResourceRecordSets Only**   
Enter a fully qualified domain name, for example, `www.example.com`\. You can optionally include a trailing dot\. If you omit the trailing dot, Amazon Route 53 assumes that the domain name that you specify is fully qualified\. This means that Route 53 treats `www.example.com` \(without a trailing dot\) and `www.example.com.` \(with a trailing dot\) as identical\.  
For information about how to specify characters other than `a-z`, `0-9`, and `-` \(hyphen\) and how to specify internationalized domain names, see [DNS Domain Name Format](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DomainNameFormat.html) in the *Amazon Route 53 Developer Guide*\.  
You can use the asterisk \(\*\) wildcard to replace the leftmost label in a domain name, for example, `*.example.com`\. Note the following:  
+ The \* must replace the entire label\. For example, you can't specify `*prod.example.com` or `prod*.example.com`\.
+ The \* can't replace any of the middle labels, for example, marketing\.\*\.example\.com\.
+ If you include \* in any position other than the leftmost label in a domain name, DNS treats it as an \* character \(ASCII 42\), not as a wildcard\.
**Important**  
You can't use the \* wildcard for resource records sets that have a type of NS\.
You can use the \* wildcard as the leftmost label in a domain name, for example, `*.example.com`\. You can't use an \* for one of the middle labels, for example, `marketing.*.example.com`\. In addition, the \* must replace the entire label; for example, you can't specify `prod*.example.com`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-route53-recordset-region"></a>
 *Latency\-based resource record sets only:* The Amazon EC2 Region where you created the resource that this resource record set refers to\. The resource typically is an AWS resource, such as an EC2 instance or an ELB load balancer, and is referred to by an IP address or a DNS domain name, depending on the record type\.  
Although creating latency and latency alias resource record sets in a private hosted zone is allowed, it's not supported\.
When Amazon Route 53 receives a DNS query for a domain name and type for which you have created latency resource record sets, Route 53 selects the latency resource record set that has the lowest latency between the end user and the associated Amazon EC2 Region\. Route 53 then returns the value that is associated with the selected resource record set\.  
Note the following:  
+ You can only specify one `ResourceRecord` per latency resource record set\.
+ You can only create one latency resource record set for each Amazon EC2 Region\.
+ You aren't required to create latency resource record sets for all Amazon EC2 Regions\. Route 53 will choose the region with the best latency from among the regions that you create latency resource record sets for\.
+ You can't create non\-latency resource record sets that have the same values for the `Name` and `Type` elements as latency resource record sets\.
*Required*: No  
*Type*: String  
*Allowed values*: `af-south-1 | ap-east-1 | ap-northeast-1 | ap-northeast-2 | ap-northeast-3 | ap-south-1 | ap-southeast-1 | ap-southeast-2 | ca-central-1 | cn-north-1 | cn-northwest-1 | eu-central-1 | eu-north-1 | eu-south-1 | eu-west-1 | eu-west-2 | eu-west-3 | me-south-1 | sa-east-1 | us-east-1 | us-east-2 | us-west-1 | us-west-2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceRecords`  <a name="cfn-route53-recordset-resourcerecords"></a>
Information about the records that you want to create\. Each record should be in the format appropriate for the record type specified by the `Type` property\. For information about different record types and their record formats, see [Values That You Specify When You Create or Edit Amazon Route 53 Records](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-values.html) in the *Amazon Route 53 Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SetIdentifier`  <a name="cfn-route53-recordset-setidentifier"></a>
 *Resource record sets that have a routing policy other than simple:* An identifier that differentiates among multiple resource record sets that have the same combination of name and type, such as multiple weighted resource record sets named acme\.example\.com that have a type of A\. In a group of resource record sets that have the same name and type, the value of `SetIdentifier` must be unique for each resource record set\.   
For information about routing policies, see [Choosing a Routing Policy](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html) in the *Amazon Route 53 Developer Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TTL`  <a name="cfn-route53-recordset-ttl"></a>
The resource record cache time to live \(TTL\), in seconds\. Note the following:  
+ If you're creating or updating an alias resource record set, omit `TTL`\. Amazon Route 53 uses the value of `TTL` for the alias target\. 
+ If you're associating this resource record set with a health check \(if you're adding a `HealthCheckId` element\), we recommend that you specify a `TTL` of 60 seconds or less so clients respond quickly to changes in health status\.
+ All of the resource record sets in a group of weighted resource record sets must have the same value for `TTL`\.
+ If a group of weighted resource record sets includes one or more weighted alias resource record sets for which the alias target is an ELB load balancer, we recommend that you specify a `TTL` of 60 seconds for all of the non\-alias weighted resource record sets that have the same name and type\. Values other than 60 seconds \(the TTL for load balancers\) will change the effect of the values that you specify for `Weight`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-route53-recordset-type"></a>
The DNS record type\. For information about different record types and how data is encoded for them, see [Supported DNS Resource Record Types](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html) in the *Amazon Route 53 Developer Guide*\.  
Valid values for basic resource record sets: `A` \| `AAAA` \| `CAA` \| `CNAME` \| `DS` \|`MX` \| `NAPTR` \| `NS` \| `PTR` \| `SOA` \| `SPF` \| `SRV` \| `TXT`   
Values for weighted, latency, geolocation, and failover resource record sets: `A` \| `AAAA` \| `CAA` \| `CNAME` \| `MX` \| `NAPTR` \| `PTR` \| `SPF` \| `SRV` \| `TXT`\. When creating a group of weighted, latency, geolocation, or failover resource record sets, specify the same value for all of the resource record sets in the group\.  
Valid values for multivalue answer resource record sets: `A` \| `AAAA` \| `MX` \| `NAPTR` \| `PTR` \| `SPF` \| `SRV` \| `TXT`   
SPF records were formerly used to verify the identity of the sender of email messages\. However, we no longer recommend that you create resource record sets for which the value of `Type` is `SPF`\. RFC 7208, *Sender Policy Framework \(SPF\) for Authorizing Use of Domains in Email, Version 1*, has been updated to say, "\.\.\.\[I\]ts existence and mechanism defined in \[RFC4408\] have led to some interoperability issues\. Accordingly, its use is no longer appropriate for SPF version 1; implementations are not to use it\." In RFC 7208, see section 14\.1, [The SPF DNS Record Type](http://tools.ietf.org/html/rfc7208#section-14.1)\.
Values for alias resource record sets:  
+  **Amazon API Gateway custom regional APIs and edge\-optimized APIs:** `A` 
+  **CloudFront distributions:** `A` 

  If IPv6 is enabled for the distribution, create two resource record sets to route traffic to your distribution, one with a value of `A` and one with a value of `AAAA`\. 
+  **Amazon API Gateway environment that has a regionalized subdomain**: `A` 
+  **ELB load balancers:** `A` \| `AAAA` 
+  **Amazon S3 buckets:** `A` 
+  **Amazon Virtual Private Cloud interface VPC endpoints** `A` 
+  **Another resource record set in this hosted zone:** Specify the type of the resource record set that you're creating the alias for\. All values are supported except `NS` and `SOA`\.
**Note**  
If you're creating an alias record that has the same name as the hosted zone \(known as the zone apex\), you can't route traffic to a record for which the value of `Type` is `CNAME`\. This is because the alias record must have the same type as the record you're routing traffic to, and creating a CNAME record for the zone apex isn't supported even for an alias record\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `A | AAAA | CAA | CNAME | DS | MX | NAPTR | NS | PTR | SOA | SPF | SRV | TXT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-route53-recordset-weight"></a>
 *Weighted resource record sets only:* Among resource record sets that have the same combination of DNS name and type, a value that determines the proportion of DNS queries that Amazon Route 53 responds to using the current resource record set\. Route 53 calculates the sum of the weights for the resource record sets that have the same combination of DNS name and type\. Route 53 then responds to queries based on the ratio of a resource's weight to the total\. Note the following:  
+ You must specify a value for the `Weight` element for every weighted resource record set\.
+ You can only specify one `ResourceRecord` per weighted resource record set\.
+ You can't create latency, failover, or geolocation resource record sets that have the same values for the `Name` and `Type` elements as weighted resource record sets\.
+ You can create a maximum of 100 weighted resource record sets that have the same values for the `Name` and `Type` elements\.
+ For weighted \(but not weighted alias\) resource record sets, if you set `Weight` to `0` for a resource record set, Route 53 never responds to queries with the applicable value for that resource record set\. However, if you set `Weight` to `0` for all resource record sets that have the same combination of DNS name and type, traffic is routed to all resources with equal probability\.

  The effect of setting `Weight` to `0` is different when you associate health checks with weighted resource record sets\. For more information, see [Options for Configuring Route 53 Active\-Active and Active\-Passive Failover](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-configuring-options.html) in the *Amazon Route 53 Developer Guide*\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-recordset-1--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-recordsetgroup.html#aws-resource-route53-recordsetgroup-return-values) in the topic [AWS::Route53::RecordSetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-recordsetgroup.html) 
+  [ResourceRecordSet](https://docs.aws.amazon.com/Route53/latest/APIReference/API_ResourceRecordSet.html) in the *Amazon Route 53 API Reference*

