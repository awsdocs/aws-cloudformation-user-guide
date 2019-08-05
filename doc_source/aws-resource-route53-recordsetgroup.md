# AWS::Route53::RecordSetGroup<a name="aws-resource-route53-recordsetgroup"></a>

A complex type that contains an optional comment, the name and ID of the hosted zone that you want to make changes in, and values for the resource record sets that you want to add, update, or delete\.

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
      "[RecordSets](#cfn-route53-recordsetgroup-recordsets)" : [ [RecordSet](aws-properties-route53-recordset-1.md), ... ]
    }
}
```

### YAML<a name="aws-resource-route53-recordsetgroup-syntax.yaml"></a>

```
Type: AWS::Route53::RecordSetGroup
Properties:
  [Comment](#cfn-route53-recordsetgroup-comment): String
  [HostedZoneId](#cfn-route53-recordsetgroup-hostedzoneid): String
  [HostedZoneName](#cfn-route53-recordsetgroup-hostedzonename): String
  [RecordSets](#cfn-route53-recordsetgroup-recordsets):
    - [RecordSet](aws-properties-route53-recordset-1.md)
```

## Properties<a name="aws-resource-route53-recordsetgroup-properties"></a>

`Comment`  <a name="cfn-route53-recordsetgroup-comment"></a>
 *Optional:* Any comments you want to include about a change batch request\.
*Required*: No
*Type*: String
*Maximum*: `256`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-route53-recordsetgroup-hostedzoneid"></a>
The ID of the hosted zone that contains the resource record sets that you want to change\.
*Required*: No
*Type*: String
*Maximum*: `32`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostedZoneName`  <a name="cfn-route53-recordsetgroup-hostedzonename"></a>
The name of the hosted zone that you want to create, update, or delete resource record sets in\.
*Required*: No
*Type*: String
*Maximum*: `1024`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordSets`  <a name="cfn-route53-recordsetgroup-recordsets"></a>
A complex type that contains one `RecordSet` element for each resource record set that you want to add, update, or delete\.
*Required*: No
*Type*: List of [RecordSet](aws-properties-route53-recordset-1.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-route53-recordsetgroup-return-values"></a>

### Ref<a name="aws-resource-route53-recordsetgroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the record set group, for example, `MyRecordSetGroup`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-route53-recordsetgroup--examples"></a>

### Mapping a Route 53 A record to the public IP of an Amazon EC2 instance<a name="aws-resource-route53-recordsetgroup--examples--Mapping_a_Route_53_A_record_to_the_public_IP_of_an_Amazon_EC2_instance"></a>

#### JSON<a name="aws-resource-route53-recordsetgroup--examples--Mapping_a_Route_53_A_record_to_the_public_IP_of_an_Amazon_EC2_instance--json"></a>

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

#### YAML<a name="aws-resource-route53-recordsetgroup--examples--Mapping_a_Route_53_A_record_to_the_public_IP_of_an_Amazon_EC2_instance--yaml"></a>

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

## See Also<a name="aws-resource-route53-recordsetgroup--seealso"></a>
+ For `AWS::Route53::RecordSetGroup` examples, see [ChangeResourceRecordSets](https://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html) in the *Amazon Route 53 API Reference*
