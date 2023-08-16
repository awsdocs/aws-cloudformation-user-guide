# AWS::CloudTrail::ResourcePolicy<a name="aws-resource-cloudtrail-resourcepolicy"></a>

 Attaches a resource\-based permission policy to a CloudTrail channel that is used for an integration with an event source outside of AWS\. For more information about resource\-based policies, see [CloudTrail resource\-based policy examples](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/security_iam_resource-based-policy-examples.html) in the *CloudTrail User Guide*\. 

## Syntax<a name="aws-resource-cloudtrail-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudtrail-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::CloudTrail::ResourcePolicy",
  "Properties" : {
      "[ResourceArn](#cfn-cloudtrail-resourcepolicy-resourcearn)" : String,
      "[ResourcePolicy](#cfn-cloudtrail-resourcepolicy-resourcepolicy)" : Json
    }
}
```

### YAML<a name="aws-resource-cloudtrail-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::CloudTrail::ResourcePolicy
Properties: 
  [ResourceArn](#cfn-cloudtrail-resourcepolicy-resourcearn): String
  [ResourcePolicy](#cfn-cloudtrail-resourcepolicy-resourcepolicy): Json
```

## Properties<a name="aws-resource-cloudtrail-resourcepolicy-properties"></a>

`ResourceArn`  <a name="cfn-cloudtrail-resourcepolicy-resourcearn"></a>
 The Amazon Resource Name \(ARN\) of the CloudTrail channel attached to the resource\-based policy\. The following is the format of a resource ARN: `arn:aws:cloudtrail:us-east-2:123456789012:channel/MyChannel`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9._/\-:]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourcePolicy`  <a name="cfn-cloudtrail-resourcepolicy-resourcepolicy"></a>
 A JSON\-formatted string for an AWS resource\-based policy\.   
The following are requirements for the resource policy:  
+  Contains only one action: cloudtrail\-data:PutAuditEvents 
+  Contains at least one statement\. The policy can have a maximum of 20 statements\. 
+  Each statement contains at least one principal\. A statement can have a maximum of 50 principals\. 
*Required*: Yes  
*Type*: Json  
*Minimum*: `1`  
*Maximum*: `8192`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudtrail-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-cloudtrail-resourcepolicy-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the resource\. The resource is a combination of the resource\-based policy document and the channel ARN\.

## Examples<a name="aws-resource-cloudtrail-resourcepolicy--examples"></a>

### Example<a name="aws-resource-cloudtrail-resourcepolicy--examples--Example"></a>

The following example creates a resource policy that allows AWS account ID `111122223333` to call `PutAuditEvents` on the channel defined as the resource ARN in the policy\. For information about creating a resource policy, see [AWS CloudTrail resource\-based policy examples](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/security_iam_resource-based-policy-examples.html) in the *AWS CloudTrail User Guide*\.

#### JSON<a name="aws-resource-cloudtrail-resourcepolicy--examples--Example--json"></a>

```
{
  "Type": "AWS:CloudTrail:ResourcePolicy",
  "Properties": {
    "ResourceArn": "arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE",
    "ResourcePolicy": "{ \"Version\": \"2012-10-17\", \"Statement\": [ { \"Sid\": \"DeliverEventsThroughChannel\", \"Effect\": \"Allow\", \"Principal\": { \"AWS\": [ \"arn:aws:iam::111122223333:root\" ] }, \"Action\":\"cloudtrail-data:PutAuditEvents\", \"Resource\": \"arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE\" } ] }"
  }
}
```

#### YAML<a name="aws-resource-cloudtrail-resourcepolicy--examples--Example--yaml"></a>

```
  Type: AWS:CloudTrail:ResourcePolicy
  Properties:
    ResourceArn: "arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE"
    ResourcePolicy: "{ \"Version\": \"2012-10-17\", \"Statement\": [ { \"Sid\": \"DeliverEventsThroughChannel\", \"Effect\": \"Allow\", \"Principal\": { \"AWS\": [ \"arn:aws:iam::111122223333:root\" ] }, \"Action\":\"cloudtrail-data:PutAuditEvents\", \"Resource\": \"arn:aws:cloudtrail:us-east-1:01234567890:channel/EXAMPLE8-0558-4f7e-a06a-43969EXAMPLE\" } ] }"
```