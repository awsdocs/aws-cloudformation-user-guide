# AWS::Route53Resolver::ResolverEndpoint<a name="aws-resource-route53resolver-resolverendpoint"></a>

Creates a Resolver endpoint\. There are two types of Resolver endpoints, inbound and outbound:
+ An *inbound Resolver endpoint* forwards DNS queries to the DNS service for a VPC from your network\.
+ An *outbound Resolver endpoint* forwards DNS queries from the DNS service for a VPC to your network\.

## Syntax<a name="aws-resource-route53resolver-resolverendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverEndpoint",
  "Properties" : {
      "[Direction](#cfn-route53resolver-resolverendpoint-direction)" : String,
      "[IpAddresses](#cfn-route53resolver-resolverendpoint-ipaddresses)" : [ IpAddressRequest, ... ],
      "[Name](#cfn-route53resolver-resolverendpoint-name)" : String,
      "[SecurityGroupIds](#cfn-route53resolver-resolverendpoint-securitygroupids)" : [ String, ... ],
      "[Tags](#cfn-route53resolver-resolverendpoint-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53resolver-resolverendpoint-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::ResolverEndpoint
Properties: 
  [Direction](#cfn-route53resolver-resolverendpoint-direction): String
  [IpAddresses](#cfn-route53resolver-resolverendpoint-ipaddresses): 
    - IpAddressRequest
  [Name](#cfn-route53resolver-resolverendpoint-name): String
  [SecurityGroupIds](#cfn-route53resolver-resolverendpoint-securitygroupids): 
    - String
  [Tags](#cfn-route53resolver-resolverendpoint-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53resolver-resolverendpoint-properties"></a>

`Direction`  <a name="cfn-route53resolver-resolverendpoint-direction"></a>
Indicates whether the Resolver endpoint allows inbound or outbound DNS queries:  
+  `INBOUND`: allows DNS queries to your VPC from your network
+  `OUTBOUND`: allows DNS queries from your VPC to your network
*Required*: Yes  
*Type*: String  
*Allowed values*: `INBOUND | OUTBOUND`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpAddresses`  <a name="cfn-route53resolver-resolverendpoint-ipaddresses"></a>
The subnets and IP addresses in your VPC that DNS queries originate from \(for outbound endpoints\) or that you forward DNS queries to \(for inbound endpoints\)\. The subnet ID uniquely identifies a VPC\.   
*Required*: Yes  
*Type*: List of [IpAddressRequest](aws-properties-route53resolver-resolverendpoint-ipaddressrequest.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53resolver-resolverendpoint-name"></a>
A friendly name that lets you easily find a configuration in the Resolver dashboard in the Route 53 console\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9\-_' ']+)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-route53resolver-resolverendpoint-securitygroupids"></a>
The ID of one or more security groups that control access to this VPC\. The security group must include one or more inbound rules \(for inbound endpoints\) or outbound rules \(for outbound endpoints\)\. Inbound and outbound rules must allow TCP and UDP access\. For inbound access, open port 53\. For outbound access, open the port that you're using for DNS queries on your network\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53resolver-resolverendpoint-tags"></a>
A list of the tag keys and values that you want to associate with the endpoint\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53resolver-resolverendpoint-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverendpoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ResolverEndpoint` object\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverendpoint-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverendpoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resolver endpoint, such as `arn:aws:route53Resolver:us-east-1:123456789012:resolver-endpoint/resolver-endpoint-a1bzhi`\.

`Direction`  <a name="Direction-fn::getatt"></a>
Indicates whether the resolver endpoint allows inbound or outbound DNS queries\.

`HostVPCId`  <a name="HostVPCId-fn::getatt"></a>
The ID of the VPC that you want to create the resolver endpoint in\.

`IpAddressCount`  <a name="IpAddressCount-fn::getatt"></a>
The number of IP addresses that the resolver endpoint can use for DNS queries\.

`Name`  <a name="Name-fn::getatt"></a>
The name that you assigned to the resolver endpoint when you created the endpoint\.

`ResolverEndpointId`  <a name="ResolverEndpointId-fn::getatt"></a>
The ID of the resolver endpoint\.

## Examples<a name="aws-resource-route53resolver-resolverendpoint--examples"></a>



### Create Resolver endpoint<a name="aws-resource-route53resolver-resolverendpoint--examples--Create_Resolver_endpoint"></a>

The following example creates an Amazon Route 53 outbound resolver endpoint\. The `IpAddresses` object includes values for `SubnetId` but not for `Ip`\. This causes Route 53 Resolver to automatically choose an IP address from among the available IP addresses in the specified subnet\.

#### JSON<a name="aws-resource-route53resolver-resolverendpoint--examples--Create_Resolver_endpoint--json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverEndpoint",
  "Properties" : {
    "Direction" : "Outbound",
    "IpAddresses" : [ 
      {
        "SubnetId": "subnet-0bca4d363dexample"
      },
      {
        "SubnetId": "subnet-0cdb5e474dexample"
      }
    ],
    "Name" : "MyOutboundEndpoint",
    "SecurityGroupIds" : [ 
      "sg-071b99f42example"
    ],
    "Tags" : [
      "Key": "LineOfBusiness",
      "Value": "Engineering"
    ]
  }
}
```

#### YAML<a name="aws-resource-route53resolver-resolverendpoint--examples--Create_Resolver_endpoint--yaml"></a>

```
Type : AWS::Route53Resolver::ResolverEndpoint
Properties :
  Direction : Outbound
  IpAddresses : 
    - SubnetId: subnet-0bca4d363dexample
    - SubnetId: subnet-0cdb5e474dexample
  Name : MyOutboundEndpoint
  SecurityGroupIds : 
    - sg-071b99f42example
  Tags : 
    - 
      Key: LineOfBusiness
      Value: Engineering
```

## See also<a name="aws-resource-route53resolver-resolverendpoint--seealso"></a>
+  [ResolverEndpoint](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverEndpoint.html) in the *Amazon Route 53 API Reference* 

