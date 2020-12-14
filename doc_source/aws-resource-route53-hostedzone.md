# AWS::Route53::HostedZone<a name="aws-resource-route53-hostedzone"></a>

Creates a new public or private hosted zone\. You create records in a public hosted zone to define how you want to route traffic on the internet for a domain, such as example\.com, and its subdomains \(apex\.example\.com, acme\.example\.com\)\. You create records in a private hosted zone to define how you want to route traffic for a domain and its subdomains within one or more Amazon Virtual Private Clouds \(Amazon VPCs\)\. 

**Important**  
You can't convert a public hosted zone to a private hosted zone or vice versa\. Instead, you must create a new hosted zone with the same name and create new resource record sets\.

For more information about charges for hosted zones, see [Amazon Route 53 Pricing](http://aws.amazon.com/route53/pricing/)\.

Note the following:
+ You can't create a hosted zone for a top\-level domain \(TLD\) such as \.com\.
+ For public hosted zones, Route 53 automatically creates a default SOA record and four NS records for the zone\. For more information about SOA and NS records, see [NS and SOA Records that Route 53 Creates for a Hosted Zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/SOA-NSrecords.html) in the *Amazon Route 53 Developer Guide*\.

  If you want to use the same name servers for multiple public hosted zones, you can optionally associate a reusable delegation set with the hosted zone\. See the `DelegationSetId` element\.
+ If your domain is registered with a registrar other than Route 53, you must update the name servers with your registrar to make Route 53 the DNS service for the domain\. For more information, see [Migrating DNS Service for an Existing Domain to Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/MigratingDNS.html) in the *Amazon Route 53 Developer Guide*\. 

When you submit a `CreateHostedZone` request, the initial status of the hosted zone is `PENDING`\. For public hosted zones, this means that the NS and SOA records are not yet available on all Route 53 DNS servers\. When the NS and SOA records are available, the status of the zone changes to `INSYNC`\.

## Syntax<a name="aws-resource-route53-hostedzone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-hostedzone-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::HostedZone",
  "Properties" : {
      "[HostedZoneConfig](#cfn-route53-hostedzone-hostedzoneconfig)" : HostedZoneConfig,
      "[HostedZoneTags](#cfn-route53-hostedzone-hostedzonetags)" : [ HostedZoneTag, ... ],
      "[Name](#cfn-route53-hostedzone-name)" : String,
      "[QueryLoggingConfig](#cfn-route53-hostedzone-queryloggingconfig)" : QueryLoggingConfig,
      "[VPCs](#cfn-route53-hostedzone-vpcs)" : [ VPC, ... ]
    }
}
```

### YAML<a name="aws-resource-route53-hostedzone-syntax.yaml"></a>

```
Type: AWS::Route53::HostedZone
Properties: 
  [HostedZoneConfig](#cfn-route53-hostedzone-hostedzoneconfig): 
    HostedZoneConfig
  [HostedZoneTags](#cfn-route53-hostedzone-hostedzonetags): 
    - HostedZoneTag
  [Name](#cfn-route53-hostedzone-name): String
  [QueryLoggingConfig](#cfn-route53-hostedzone-queryloggingconfig): 
    QueryLoggingConfig
  [VPCs](#cfn-route53-hostedzone-vpcs): 
    - VPC
```

## Properties<a name="aws-resource-route53-hostedzone-properties"></a>

`HostedZoneConfig`  <a name="cfn-route53-hostedzone-hostedzoneconfig"></a>
A complex type that contains an optional comment\.  
If you don't want to specify a comment, omit the `HostedZoneConfig` and `Comment` elements\.  
*Required*: No  
*Type*: [HostedZoneConfig](aws-properties-route53-hostedzone-hostedzoneconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneTags`  <a name="cfn-route53-hostedzone-hostedzonetags"></a>
Adds, edits, or deletes tags for a health check or a hosted zone\.  
For information about using tags for cost allocation, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
*Required*: No  
*Type*: List of [HostedZoneTag](aws-properties-route53-hostedzone-hostedzonetag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53-hostedzone-name"></a>
The name of the domain\. Specify a fully qualified domain name, for example, *www\.example\.com*\. The trailing dot is optional; Amazon Route 53 assumes that the domain name is fully qualified\. This means that Route 53 treats *www\.example\.com* \(without a trailing dot\) and *www\.example\.com\.* \(with a trailing dot\) as identical\.  
If you're creating a public hosted zone, this is the name you have registered with your DNS registrar\. If your domain name is registered with a registrar other than Route 53, change the name servers for your domain to the set of `NameServers` that are returned by the `Fn::GetAtt` intrinsic function\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QueryLoggingConfig`  <a name="cfn-route53-hostedzone-queryloggingconfig"></a>
Creates a configuration for DNS query logging\. After you create a query logging configuration, Amazon Route 53 begins to publish log data to an Amazon CloudWatch Logs log group\.  
DNS query logs contain information about the queries that Route 53 receives for a specified public hosted zone, such as the following:  
+ Route 53 edge location that responded to the DNS query
+ Domain or subdomain that was requested
+ DNS record type, such as A or AAAA
+ DNS response code, such as `NoError` or `ServFail`   
Log Group and Resource Policy  
Before you create a query logging configuration, perform the following operations\.  
If you create a query logging configuration using the Route 53 console, Route 53 performs these operations automatically\.

1. Create a CloudWatch Logs log group, and make note of the ARN, which you specify when you create a query logging configuration\. Note the following:
   + You must create the log group in the us\-east\-1 region\.
   + You must use the same AWS account to create the log group and the hosted zone that you want to configure query logging for\.
   + When you create log groups for query logging, we recommend that you use a consistent prefix, for example:

      `/aws/route53/hosted zone name ` 

     In the next step, you'll create a resource policy, which controls access to one or more log groups and the associated AWS resources, such as Route 53 hosted zones\. There's a limit on the number of resource policies that you can create, so we recommend that you use a consistent prefix so you can use the same resource policy for all the log groups that you create for query logging\.

1. Create a CloudWatch Logs resource policy, and give it the permissions that Route 53 needs to create log streams and to send query logs to log streams\. For the value of `Resource`, specify the ARN for the log group that you created in the previous step\. To use the same resource policy for all the CloudWatch Logs log groups that you created for query logging configurations, replace the hosted zone name with `*`, for example:

    `arn:aws:logs:us-east-1:123412341234:log-group:/aws/route53/*` 
**Note**  
You can't use the CloudWatch console to create or edit a resource policy\. You must use the CloudWatch API, one of the AWS SDKs, or the AWS CLI\.  
Log Streams and Edge Locations  
When Route 53 finishes creating the configuration for DNS query logging, it does the following:  
+ Creates a log stream for an edge location the first time that the edge location responds to DNS queries for the specified hosted zone\. That log stream is used to log all queries that Route 53 responds to for that edge location\.
+ Begins to send query logs to the applicable log stream\.
The name of each log stream is in the following format:  
 ` hosted zone ID/edge location code `   
The edge location code is a three\-letter code and an arbitrarily assigned number, for example, DFW3\. The three\-letter code typically corresponds with the International Air Transport Association airport code for an airport near the edge location\. \(These abbreviations might change in the future\.\) For a list of edge locations, see "The Route 53 Global Network" on the [Route 53 Product Details](http://aws.amazon.com/route53/details/) page\.  
Queries That Are Logged  
Query logs contain only the queries that DNS resolvers forward to Route 53\. If a DNS resolver has already cached the response to a query \(such as the IP address for a load balancer for example\.com\), the resolver will continue to return the cached response\. It doesn't forward another query to Route 53 until the TTL for the corresponding resource record set expires\. Depending on how many DNS queries are submitted for a resource record set, and depending on the TTL for that resource record set, query logs might contain information about only one query out of every several thousand queries that are submitted to DNS\. For more information about how DNS works, see [Routing Internet Traffic to Your Website or Web Application](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-dns-service.html) in the *Amazon Route 53 Developer Guide*\.  
Log File Format  
For a list of the values in each query log and the format of each value, see [Logging DNS Queries](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/query-logs.html) in the *Amazon Route 53 Developer Guide*\.  
Pricing  
For information about charges for query logs, see [Amazon CloudWatch Pricing](http://aws.amazon.com/cloudwatch/pricing/)\.  
How to Stop Logging  
If you want Route 53 to stop sending query logs to CloudWatch Logs, delete the query logging configuration\. For more information, see [DeleteQueryLoggingConfig](https://docs.aws.amazon.com/Route53/latest/APIReference/API_DeleteQueryLoggingConfig.html)\.
*Required*: No  
*Type*: [QueryLoggingConfig](aws-properties-route53-hostedzone-queryloggingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCs`  <a name="cfn-route53-hostedzone-vpcs"></a>
*Private hosted zones:* A complex type that contains information about the VPCs that are associated with the specified hosted zone\.  
For public hosted zones, omit `VPCs`, `VPCId`, and `VPCRegion`\.
*Required*: No  
*Type*: List of [VPC](aws-properties-route53-hostedzone-vpc.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53-hostedzone-return-values"></a>

### Ref<a name="aws-resource-route53-hostedzone-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the hosted zone ID, such as `Z23ABC4XYZL05B`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53-hostedzone-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53-hostedzone-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`NameServers`  <a name="NameServers-fn::getatt"></a>
Returns the set of name servers for the specific hosted zone\. For example: `ns1.example.com`\.  
This attribute is not supported for private hosted zones\.

## Examples<a name="aws-resource-route53-hostedzone--examples"></a>



### Creating a private hosted zone<a name="aws-resource-route53-hostedzone--examples--Creating_a_private_hosted_zone"></a>

The following template snippet creates a private hosted zone for the example\.com domain\.

#### JSON<a name="aws-resource-route53-hostedzone--examples--Creating_a_private_hosted_zone--json"></a>

```
{
   "DNS": {
      "Type": "AWS: : Route53: : HostedZone",
      "Properties": {
         "HostedZoneConfig": {
            "Comment": "Myhostedzoneforexample.com"
         },
         "Name": "example.com",
         "VPCs": [
            {
               "VPCId": "vpc-abcd1234",
               "VPCRegion": "ap-northeast-1"
            },
            {
               "VPCId": "vpc-efgh5678",
               "VPCRegion": "us-west-2"
            }
         ],
         "HostedZoneTags": [
            {
               "Key": "SampleKey1",
               "Value": "SampleValue1"
            },
            {
               "Key": "SampleKey2",
               "Value": "SampleValue2"
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-route53-hostedzone--examples--Creating_a_private_hosted_zone--yaml"></a>

```
DNS: 
  Type: "AWS::Route53::HostedZone"
  Properties: 
    HostedZoneConfig: 
      Comment: 'My hosted zone for example.com'
    Name: 'example.com'
    VPCs: 
      - 
        VPCId: 'vpc-abcd1234'
        VPCRegion: 'ap-northeast-1'
      - 
        VPCId: 'vpc-efgh5678'
        VPCRegion: 'us-west-2'
    HostedZoneTags: 
      - 
        Key: 'SampleKey1'
        Value: 'SampleValue1'
      - 
        Key: 'SampleKey2'
        Value: 'SampleValue2'
```

## See also<a name="aws-resource-route53-hostedzone--seealso"></a>
+  [CreateHostedZone](https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateHostedZone.html) in the *Amazon Route 53 API Reference*

