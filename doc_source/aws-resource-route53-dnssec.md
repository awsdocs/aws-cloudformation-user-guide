# AWS::Route53::DNSSEC<a name="aws-resource-route53-dnssec"></a>

The `AWS::Route53::DNSSEC` resource is used to enable DNSSEC signing in a hosted zone\.

## Syntax<a name="aws-resource-route53-dnssec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-dnssec-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::DNSSEC",
  "Properties" : {
      "[HostedZoneId](#cfn-route53-dnssec-hostedzoneid)" : String
    }
}
```

### YAML<a name="aws-resource-route53-dnssec-syntax.yaml"></a>

```
Type: AWS::Route53::DNSSEC
Properties: 
  [HostedZoneId](#cfn-route53-dnssec-hostedzoneid): String
```

## Properties<a name="aws-resource-route53-dnssec-properties"></a>

`HostedZoneId`  <a name="cfn-route53-dnssec-hostedzoneid"></a>
A unique string \(ID\) that is used to identify a hosted zone\. For example: `Z00001111A1ABCaaABC11`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53-dnssec-return-values"></a>

### Ref<a name="aws-resource-route53-dnssec-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the hosted zone ID\. For example:

 `{ "Ref": "Z00001111A1ABCaaABC11" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.