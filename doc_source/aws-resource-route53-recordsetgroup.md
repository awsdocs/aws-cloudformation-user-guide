# AWS::Route53::RecordSetGroup<a name="aws-resource-route53-recordsetgroup"></a>

A complex type that contains an optional comment, the name and ID of the hosted zone that you want to make changes in, and values for the records that you want to create\.

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
      "[RecordSets](#cfn-route53-recordsetgroup-recordsets)" : [ RecordSet, ... ]
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
    - RecordSet
```

## Properties<a name="aws-resource-route53-recordsetgroup-properties"></a>

`Comment`  <a name="cfn-route53-recordsetgroup-comment"></a>
 *Optional:* Any comments you want to include about a change batch request\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostedZoneId`  <a name="cfn-route53-recordsetgroup-hostedzoneid"></a>
The ID of the hosted zone that you want to create records in\.  
Specify either `HostedZoneName` or `HostedZoneId`, but not both\. If you have multiple hosted zones with the same domain name, you must specify the hosted zone using `HostedZoneId`\.   
*Required*: No  
*Type*: String  
*Maximum*: `32`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostedZoneName`  <a name="cfn-route53-recordsetgroup-hostedzonename"></a>
The name of the hosted zone that you want to create records in\.  
When you create a stack using an `AWS::Route53::RecordSet` that specifies `HostedZoneName`, AWS CloudFormation attempts to find a hosted zone whose name matches the `HostedZoneName`\. If AWS CloudFormation can't find a hosted zone with a matching domain name, or if there is more than one hosted zone with the specified domain name, AWS CloudFormation will not create the stack\.   
Specify either `HostedZoneName` or `HostedZoneId`, but not both\. If you have multiple hosted zones with the same domain name, you must specify the hosted zone using `HostedZoneId`\.   
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordSets`  <a name="cfn-route53-recordsetgroup-recordsets"></a>
A complex type that contains one `RecordSet` element for each record that you want to create\.  
*Required*: No  
*Type*: List of [RecordSet](aws-properties-route53-recordset-1.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53-recordsetgroup-return-values"></a>

### Ref<a name="aws-resource-route53-recordsetgroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the record set group, for example, `MyRecordSetGroup`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-route53-recordsetgroup--examples"></a>

For more examples, see [Route 53 Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-route53.html)\.

### Creating records for a mail server<a name="aws-resource-route53-recordsetgroup--examples--Creating_records_for_a_mail_server"></a>

The following example shows how to create three records for a mail server:
+ An A record that specifies the IP address for the mail server\.
+ An MX record that routes email to that server\.
+ A TXT record that contains an SPF string, which is used to identify the sender of email messages\. SPF records are no longer recommended\. For more information, see [SPF Record Type](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html#SPFFormat) in the *Amazon Route 53 Developer Guide*\.

#### JSON<a name="aws-resource-route53-recordsetgroup--examples--Creating_records_for_a_mail_server--json"></a>

```
{
   "myExampleDotComEmailServer": {
      "Type": "AWS::Route53::RecordSetGroup",
      "Properties": {
         "Comment": "Creating records for mail server",
         "HostedZoneId": "Z1PA6795UKMFR9",
         "RecordSets": [
            {
               "Name": "mail.example.com.",
               "Type": "A",
               "TTL": "900",
               "ResourceRecords": [
                  "192.0.2.44"
               ]
            },
            {
               "Name": "mail.example.com.",
               "Type": "MX",
               "TTL": "900",
               "ResourceRecords": [
                  "10 mail.example.com"
               ]
            },
            {
               "Name": "mail.example.com.",
               "Type": "TXT",
               "TTL": "900",
               "ResourceRecords": [
                  "\"v=spf1 ip4:203.0.113.0/30 -all\""
               ]
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-route53-recordsetgroup--examples--Creating_records_for_a_mail_server--yaml"></a>

```
myExampleDotComEmailServer:
  Type: AWS::Route53::RecordSetGroup
  Properties:
    Comment: Creating records for mail server
    HostedZoneId: Z1PA6795UKMFR9
    RecordSets:
    - Name: mail.example.com.
      ResourceRecords: 
      - 192.0.2.44
      TTL: '900'
      Type: A
    - Name: mail.example.com.
      ResourceRecords: 
      - '10 mail.example.com'
      TTL: '900'
      Type: MX
    - Name: mail.example.com.
      ResourceRecords: 
      - '"v=spf1 ip4:203.0.113.0/30 -all"'
      TTL: '900'
      Type: TXT
```

## See also<a name="aws-resource-route53-recordsetgroup--seealso"></a>
+ For `AWS::Route53::RecordSetGroup` examples, see [ChangeResourceRecordSets](https://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html) in the *Amazon Route 53 API Reference*

