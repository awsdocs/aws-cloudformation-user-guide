# AWS::Route53Resolver::OutpostResolver<a name="aws-resource-route53resolver-outpostresolver"></a>

Creates a Amazon Route 53 Resolver on an Outpost\.

## Syntax<a name="aws-resource-route53resolver-outpostresolver-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-outpostresolver-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::OutpostResolver",
  "Properties" : {
      "[InstanceCount](#cfn-route53resolver-outpostresolver-instancecount)" : Integer,
      "[Name](#cfn-route53resolver-outpostresolver-name)" : String,
      "[OutpostArn](#cfn-route53resolver-outpostresolver-outpostarn)" : String,
      "[PreferredInstanceType](#cfn-route53resolver-outpostresolver-preferredinstancetype)" : String,
      "[Tags](#cfn-route53resolver-outpostresolver-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53resolver-outpostresolver-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::OutpostResolver
Properties: 
  [InstanceCount](#cfn-route53resolver-outpostresolver-instancecount): Integer
  [Name](#cfn-route53resolver-outpostresolver-name): String
  [OutpostArn](#cfn-route53resolver-outpostresolver-outpostarn): String
  [PreferredInstanceType](#cfn-route53resolver-outpostresolver-preferredinstancetype): String
  [Tags](#cfn-route53resolver-outpostresolver-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53resolver-outpostresolver-properties"></a>

`InstanceCount`  <a name="cfn-route53resolver-outpostresolver-instancecount"></a>
Amazon EC2 instance count for the Resolver on the Outpost\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53resolver-outpostresolver-name"></a>
Name of the Resolver\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostArn`  <a name="cfn-route53resolver-outpostresolver-outpostarn"></a>
The ARN \(Amazon Resource Name\) for the Outpost\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^arn:aws([a-z-]+)?:outposts:[a-z\d-]+:\d{12}:outpost/op-[a-f0-9]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredInstanceType`  <a name="cfn-route53resolver-outpostresolver-preferredinstancetype"></a>
 The Amazon EC2 instance type\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-route53resolver-outpostresolver-tags"></a>
A key value pair that helps you identify a Route 53 Resolver\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53resolver-outpostresolver-return-values"></a>

### Ref<a name="aws-resource-route53resolver-outpostresolver-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns returns the `Id` of the Outpost Resolver\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-outpostresolver-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-outpostresolver-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN \(Amazon Resource Name\) for the Resolver on an Outpost\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The date and time that the Outpost Resolver was created, in Unix time format and Coordinated Universal Time \(UTC\)\.

`CreatorRequestId`  <a name="CreatorRequestId-fn::getatt"></a>
A unique string that identifies the request that created the Resolver endpoint\. The `CreatorRequestId` allows failed requests to be retried without the risk of running the operation twice\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the Resolver on Outpost\.

`ModificationTime`  <a name="ModificationTime-fn::getatt"></a>
The date and time that the Outpost Resolver was modified, in Unix time format and Coordinated Universal Time \(UTC\)\.

`Status`  <a name="Status-fn::getatt"></a>
Status of the Resolver\.  
Valid Values: CREATING \| OPERATIONAL \| UPDATING \| DELETING \| ACTION\_NEEDED \| FAILED\_CREATION \| FAILED\_DELETION\.

`StatusMessage`  <a name="StatusMessage-fn::getatt"></a>
A detailed description of the Resolver\.

## Examples<a name="aws-resource-route53resolver-outpostresolver--examples"></a>



### Create a Resolver on Outpost<a name="aws-resource-route53resolver-outpostresolver--examples--Create_a_Resolver_on_Outpost"></a>

The following example creates a Amazon Route 53 Resolver on an AWS Outposts\.

#### JSON<a name="aws-resource-route53resolver-outpostresolver--examples--Create_a_Resolver_on_Outpost--json"></a>

```
{
"Type": "AWS::Route53Resolver::OutpostResolver",
"Properties": {
    "Name": "SampleOutpostResolver",
    "InstanceCount": 4,
    "OutpostArn": "arn:aws:outposts:us-west-2:123456789012:outpost/op-12345678901234567",
    "PreferredInstanceType": "m5.large",
    "Tags": [
        {
            "Key": "keyname1",
            "Value": "value1"
        },
        {
            "Key": "keyname2",
            "Value": "value2"
        }
      ]
    }
}
```

#### YAML<a name="aws-resource-route53resolver-outpostresolver--examples--Create_a_Resolver_on_Outpost--yaml"></a>

```
Type: AWS::Route53Resolver::OutpostResolver
Properties:
  Name: SampleOutpostResolver
  InstanceCount: 4
  OutpostArn: arn:aws:outposts:us-west-2:123456789012:outpost/op-12345678901234567
  PreferredInstanceType: m5.large
  Tags:
    - Key: "keyname1"
      Value: "value1"
    - Key: "keyname2"
      Value: "value2"
```