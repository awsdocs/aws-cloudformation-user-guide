# AWS::Route53::RecordSetGroup<a name="aws-properties-route53-recordsetgroup"></a>

The `AWS::Route53::RecordSetGroup` resource creates record sets for a hosted zone\. For more information about constraints and values for each property, see [POST CreateHostedZone](http://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateHostedZone.html) for hosted zones and [POST ChangeResourceRecordSet](http://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html) for resource record sets\.

**Topics**
+ [Syntax](#aws-resource-route53-recordsetgroup-syntax)
+ [Properties](#w3ab2c21c10e1028b9)
+ [Return Value](#w3ab2c21c10e1028c11)
+ [Examples](#w3ab2c21c10e1028c13)

## Syntax<a name="aws-resource-route53-recordsetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-recordsetgroup-syntax.json"></a>

```
{
   "Type" : "AWS::Route53::RecordSetGroup",
   "Properties" : {
      "[Comment](#cfn-route53-recordsetgroup-comment)" : String,
      "[HostedZoneId](#cfn-route53-recordsetgroup-hostedzoneid)" : String,
      "[HostedZoneName](#cfn-route53-recordsetgroup-hostedzonename)" : String,
      "[RecordSets](#cfn-route53-recordsetgroup-recordsets)" : [ RecordSet1, ... ]
   }
}
```

### YAML<a name="aws-resource-route53-recordsetgroup-syntax.yaml"></a>

```
Type: "AWS::Route53::RecordSetGroup"
Properties: 
  [Comment](#cfn-route53-recordsetgroup-comment): String
  [HostedZoneId](#cfn-route53-recordsetgroup-hostedzoneid): String
  [HostedZoneName](#cfn-route53-recordsetgroup-hostedzonename): String
  [RecordSets](#cfn-route53-recordsetgroup-recordsets):
    - RecordSet1
```

## Properties<a name="w3ab2c21c10e1028b9"></a>

`Comment`  <a name="cfn-route53-recordsetgroup-comment"></a>
Any comments you want to include about the hosted zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HostedZoneId`  <a name="cfn-route53-recordsetgroup-hostedzoneid"></a>
The ID of the hosted zone\.  
*Required*: Conditional: You must specify either the `HostedZoneName` or `HostedZoneId`, but you cannot specify both\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`HostedZoneName`  <a name="cfn-route53-recordsetgroup-hostedzonename"></a>
The name of the domain for the hosted zone where you want to add the record set\.  
When you create a stack using an `AWS::Route53::RecordSet` that specifies `HostedZoneName`, AWS CloudFormation attempts to find a hosted zone whose name matches the `HostedZoneName`\. If AWS CloudFormation cannot find a hosted zone with a matching domain name, or if there is more than one hosted zone with the specified domain name, AWS CloudFormation will not create the stack\.  
If you have multiple hosted zones with the same domain name, you must explicitly specify the hosted zone using `HostedZoneId`\.  
*Required*: Conditional\. You must specify either the `HostedZoneName` or `HostedZoneId`, but you cannot specify both\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RecordSets`  <a name="cfn-route53-recordsetgroup-recordsets"></a>
List of resource record sets to add\. The maximum number of records is 1,000\.  
*Required*: Yes  
*Type*:: List of [AWS::Route53::RecordSet](aws-properties-route53-recordset.md) objects, as shown in the following example:   

```
"RecordSets" : [
  {
    "Name" : "mysite.example.com.",
    "Type" : "CNAME",
    "TTL" : "900",
    "SetIdentifier" : "Frontend One",
    "Weight" : "4",
    "ResourceRecords" : ["example-ec2.amazonaws.com"]
  },
  {
    "Name" : "mysite.example.com.",
    "Type" : "CNAME",
    "TTL" : "900",
    "SetIdentifier" : "Frontend Two",
    "Weight" : "6",
    "ResourceRecords" : ["example-ec2-larger.amazonaws.com"]
  }
]
```
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1028c11"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyRecordSetGroup" }
```

For the resource with the logical ID "MyRecordSetGroup", `Ref` will return the AWS resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1028c13"></a>

For AWS::Route53::RecordSetGroup snippets, see [Route 53 Template Snippets](quickref-route53.md)\.