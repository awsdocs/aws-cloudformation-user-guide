# AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation"></a>

The AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation resource is a configuration for DNS query logging\. After you create a query logging configuration, Amazon Route 53 begins to publish log data to an Amazon CloudWatch Logs log group\.

## Syntax<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation",
  "Properties" : {
      "[ResolverQueryLogConfigId](#cfn-route53resolver-resolverqueryloggingconfigassociation-resolverquerylogconfigid)" : String,
      "[ResourceId](#cfn-route53resolver-resolverqueryloggingconfigassociation-resourceid)" : String
    }
}
```

### YAML<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation
Properties: 
  [ResolverQueryLogConfigId](#cfn-route53resolver-resolverqueryloggingconfigassociation-resolverquerylogconfigid): String
  [ResourceId](#cfn-route53resolver-resolverqueryloggingconfigassociation-resourceid): String
```

## Properties<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-properties"></a>

`ResolverQueryLogConfigId`  <a name="cfn-route53resolver-resolverqueryloggingconfigassociation-resolverquerylogconfigid"></a>
The ID of the query logging configuration that a VPC is associated with\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceId`  <a name="cfn-route53resolver-resolverqueryloggingconfigassociation-resourceid"></a>
The ID of the Amazon VPC that is associated with the query logging configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the configuration for DNS query logging\.

For example: `{ "Ref": "rqlca-1111222233334444" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverqueryloggingconfigassociation-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The date and time that the VPC was associated with the query logging configuration, in Unix time format and Coordinated Universal Time \(UTC\)\.

`Error`  <a name="Error-fn::getatt"></a>
If the value of `Status` is `FAILED`, the value of `Error` indicates the cause:  
+ `DESTINATION_NOT_FOUND`: The specified destination \(for example, an Amazon S3 bucket\) was deleted\.
+ `ACCESS_DENIED`: Permissions don't allow sending logs to the destination\.
If the value of `Status` is a value other than `FAILED`, `Error` is null\. 

`ErrorMessage`  <a name="ErrorMessage-fn::getatt"></a>
Contains additional information about the error\. If the value or `Error` is null, the value of `ErrorMessage` is also null\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the query logging association\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the specified query logging association\. Valid values include the following:  
+ `CREATING`: Resolver is creating an association between an Amazon Virtual Private Cloud \(Amazon VPC\) and a query logging configuration\.
+ `CREATED`: The association between an Amazon VPC and a query logging configuration was successfully created\. Resolver is logging queries that originate in the specified VPC\.
+ `DELETING`: Resolver is deleting this query logging association\.
+ `FAILED`: Resolver either couldn't create or couldn't delete the query logging association\.