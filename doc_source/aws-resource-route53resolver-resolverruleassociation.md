# AWS::Route53Resolver::ResolverRuleAssociation<a name="aws-resource-route53resolver-resolverruleassociation"></a>

In the response to an [AssociateResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_AssociateResolverRule.html), [DisassociateResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_DisassociateResolverRule.html), or [ListResolverRuleAssociations](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ListResolverRuleAssociations.html) request, provides information about an association between a resolver rule and a VPC\. The association determines which DNS queries that originate in the VPC are forwarded to your network\. 

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
Type: AWS::Route53Resolver::ResolverRuleAssociation
Properties: 
  [Name](#cfn-route53resolver-resolverruleassociation-name): String
  [ResolverRuleId](#cfn-route53resolver-resolverruleassociation-resolverruleid): String
  [VPCId](#cfn-route53resolver-resolverruleassociation-vpcid): String
```

## Properties<a name="aws-resource-route53resolver-resolverruleassociation-properties"></a>

`Name`  <a name="cfn-route53resolver-resolverruleassociation-name"></a>
The name of an association between a Resolver rule and a VPC\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9\-_' ']+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResolverRuleId`  <a name="cfn-route53resolver-resolverruleassociation-resolverruleid"></a>
The ID of the Resolver rule that you associated with the VPC that is specified by `VPCId`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VPCId`  <a name="cfn-route53resolver-resolverruleassociation-vpcid"></a>
The ID of the VPC that you associated the Resolver rule with\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53resolver-resolverruleassociation-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverruleassociation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ResolverRuleAssociationId`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverruleassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverruleassociation-return-values-fn--getatt-fn--getatt"></a>

`Name`  <a name="Name-fn::getatt"></a>
The name of an association between a resolver rule and a VPC, such as `test.example.com in beta VPC`\.

`ResolverRuleAssociationId`  <a name="ResolverRuleAssociationId-fn::getatt"></a>
The ID of the resolver rule association that you want to get information about, such as `rslvr-rrassoc-97242eaf88example`\.

`ResolverRuleId`  <a name="ResolverRuleId-fn::getatt"></a>
The ID of the resolver rule that you associated with the VPC that is specified by `VPCId`, such as `rslvr-rr-5328a0899example`\.

`VPCId`  <a name="VPCId-fn::getatt"></a>
The ID of the VPC that you associated the resolver rule with, such as `vpc-03cf94c75cexample`\.

## See also<a name="aws-resource-route53resolver-resolverruleassociation--seealso"></a>
+  [ResolverRuleAssociation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRuleAssociation.html) in the *Amazon Route 53 API Reference* 

