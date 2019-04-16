# AWS::Route53Resolver::ResolverRuleAssociation<a name="aws-resource-route53resolver-resolverruleassociation"></a>

The `AWS::Route53Resolver::ResolverRuleAssociation` resource contains information about an association between a resolver rule and a VPC\. For more information, see [ResolverRuleAssociation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRuleAssociation.html) in the *Amazon Route 53 API Reference*\. 

## Syntax<a name="aws-resource-route53resolver-resolverruleassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverruleassociation-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverRuleAssociation",
  "Properties" : {
    "[Name](#cfn-route53resolver-resolverruleassociation-name)" : String,
    "[ResolverRuleId](#cfn-route53resolver-resolverruleassociation-resolverruleid)" : String,
    "[VPCId](#cfn-route53resolver-resolverruleassociation-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-route53resolver-resolverruleassociation-syntax.yaml"></a>

```
Type: "AWS::Route53Resolver::ResolverRuleAssociation"
Properties:
  [Name](#cfn-route53resolver-resolverruleassociation-name): String
  [ResolverRuleId](#cfn-route53resolver-resolverruleassociation-resolverruleid): String
  [VPCId](#cfn-route53resolver-resolverruleassociation-vpcid): String
```

## Properties<a name="aws-resource-route53resolver-resolverruleassociation-properties"></a>

`Name`  <a name="cfn-route53resolver-resolverruleassociation-name"></a>
The name of an association between a resolver rule and a VPC\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResolverRuleId`  <a name="cfn-route53resolver-resolverruleassociation-resolverruleid"></a>
The ID of the resolver rule that you associated with the VPC that is specified by `VPCId`\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VPCId`  <a name="cfn-route53resolver-resolverruleassociation-vpcid"></a>
The ID of the VPC that you associated the resolver rule with\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-route53resolver-resolverruleassociation-returnvalues"></a>

### Ref<a name="aws-resource-route53resolver-resolverruleassociation-ref"></a>

When you pass the logical ID of an `AWS::Route53Resolver::ResolverRuleAssociation` resource to the intrinsic `Ref` function, the function returns the `ResolverRuleAssociationId`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverruleassociation-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Name`  
The name of an association between a resolver rule and a VPC, such as `test.example.com in beta VPC`\.

`ResolverRuleAssociationId`  
The ID of the resolver rule association that you want to get information about, such as `rslvr-rrassoc-97242eaf88example`\.

`ResolverRuleId`  
The ID of the resolver rule that you associated with the VPC that is specified by `VPCId`, such as `rslvr-rr-5328a0899example`\.

`VPCId`  
The ID of the VPC that you associated the resolver rule with, such as `vpc-03cf94c75cexample`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## See Also<a name="aws-resource-route53resolver-resolverruleassociation-seealso"></a>
+  [ResolverRuleAssociation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRuleAssociation.html) in the *Amazon Route 53 API Reference*\. 