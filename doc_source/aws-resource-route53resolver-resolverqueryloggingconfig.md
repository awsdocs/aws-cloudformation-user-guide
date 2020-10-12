# AWS::Route53Resolver::ResolverQueryLoggingConfig<a name="aws-resource-route53resolver-resolverqueryloggingconfig"></a>

The AWS::Route53Resolver::ResolverQueryLoggingConfig resource is a complex type that contains settings for one query logging configuration\.

## Syntax<a name="aws-resource-route53resolver-resolverqueryloggingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverqueryloggingconfig-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverQueryLoggingConfig",
  "Properties" : {
      "[DestinationArn](#cfn-route53resolver-resolverqueryloggingconfig-destinationarn)" : String,
      "[Name](#cfn-route53resolver-resolverqueryloggingconfig-name)" : String
    }
}
```

### YAML<a name="aws-resource-route53resolver-resolverqueryloggingconfig-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::ResolverQueryLoggingConfig
Properties: 
  [DestinationArn](#cfn-route53resolver-resolverqueryloggingconfig-destinationarn): String
  [Name](#cfn-route53resolver-resolverqueryloggingconfig-name): String
```

## Properties<a name="aws-resource-route53resolver-resolverqueryloggingconfig-properties"></a>

`DestinationArn`  <a name="cfn-route53resolver-resolverqueryloggingconfig-destinationarn"></a>
The ARN of the resource that you want Resolver to send query logs: an Amazon S3 bucket, a CloudWatch Logs log group, or a Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `600`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-route53resolver-resolverqueryloggingconfig-name"></a>
The name of the query logging configuration\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9\-_' ']+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53resolver-resolverqueryloggingconfig-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverqueryloggingconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the resource that contains settings for one query logging configuration\.

For example: `{ "Ref": "rqlc-1111222233334444" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverqueryloggingconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverqueryloggingconfig-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the query logging configuration\.

`AssociationCount`  <a name="AssociationCount-fn::getatt"></a>
The number of VPCs that are associated with the query logging configuration\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The date and time that the query logging configuration was created, in Unix time format and Coordinated Universal Time \(UTC\)\.

`CreatorRequestId`  <a name="CreatorRequestId-fn::getatt"></a>
A unique string that identifies the request that created the query logging configuration\. The `CreatorRequestId` allows failed requests to be retried without the risk of running the operation twice\.

`Id`  <a name="Id-fn::getatt"></a>
The ID for the query logging configuration\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The AWS account ID for the account that created the query logging configuration\. 

`ShareStatus`  <a name="ShareStatus-fn::getatt"></a>
An indication of whether the query logging configuration is shared with other AWS accounts, or was shared with the current account by another AWS account\. Sharing is configured through AWS Resource Access Manager \(AWS RAM\)\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the specified query logging configuration\. Valid values include the following:  
+ `CREATING`: Resolver is creating the query logging configuration\.
+ `CREATED`: The query logging configuration was successfully created\. Resolver is logging queries that originate in the specified VPC\.
+ `DELETING`: Resolver is deleting this query logging configuration\.
+ `FAILED`: Resolver can't deliver logs to the location that is specified in the query logging configuration\. Here are two common causes:
  + The specified destination \(for example, an Amazon S3 bucket\) was deleted\.
  + Permissions don't allow sending logs to the destination\.