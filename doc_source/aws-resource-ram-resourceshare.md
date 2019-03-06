# AWS::RAM::ResourceShare<a name="aws-resource-ram-resourceshare"></a>

The `AWS::RAM::ResourceShare` resource is used to create, update, and delete an Amazon ResourceShare\. For more information, see [ResourceShare](https://docs.aws.amazon.com/ram/latest/APIReference/API_ResourceShare.html) in the *AWS RAM API Reference*\. 

## Syntax<a name="aws-resource-ram-resourceshare-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ram-resourceshare-syntax.json"></a>

```
{
  "Type" : "AWS::RAM::ResourceShare",
  "Properties" : {
    "[AllowExternalPrincipals](#cfn-ram-resourceshare-allowexternalprincipals)" : Boolean,
    "[Name](#cfn-ram-resourceshare-name)" : String,
    "[Principals](#cfn-ram-resourceshare-principals)" : [ String, ... ],
    "[ResourceArns](#cfn-ram-resourceshare-resourcearns)" : [ String, ... ],
    "[Tags](#cfn-ram-resourceshare-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-ram-resourceshare-syntax.yaml"></a>

```
Type: "AWS::RAM::ResourceShare"
Properties:
  [AllowExternalPrincipals](#cfn-ram-resourceshare-allowexternalprincipals): Boolean
  [Name](#cfn-ram-resourceshare-name): String
  [Principals](#cfn-ram-resourceshare-principals): 
    - String
  [ResourceArns](#cfn-ram-resourceshare-resourcearns): 
    - String
  [Tags](#cfn-ram-resourceshare-tags): 
    - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-ram-resourceshare-properties"></a>

`AllowExternalPrincipals`  <a name="cfn-ram-resourceshare-allowexternalprincipals"></a>
Indicates whether principals outside of your organization are allowed in this ResourceShare\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ram-resourceshare-name"></a>
A descriptive name for the ResourceShare\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Principals`  <a name="cfn-ram-resourceshare-principals"></a>
A list of account IDs, organizational unit ARNs, and organization ARN to put into the ResourceShare\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceArns`  <a name="cfn-ram-resourceshare-resourcearns"></a>
The resource ARNs to put into the ResourceShare\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-ram-resourceshare-tags"></a>
The tags on this ResourceShare\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ram-resourceshare-returnvalues"></a>

### Ref<a name="aws-resource-ram-resourceshare-ref"></a>

When you pass the logical ID of an `AWS::RAM::ResourceShare` resource to the intrinsic `Ref` function, the function returns the ARN of the created Amazon ResourceShare, such as `arn:aws:ram:us-east-1:123456789012:resource-share/12345678-1234-1234-1234-12345678`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-ram-resourceshare-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the resource share, such as `arn:aws:ram:us-east-1:123456789012:resource-share/12345678-1234-1234-1234-12345678`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-ram-resourceshare-examples"></a>

### ResourceShare creation example<a name="aws-resource-ram-resourceshare-example1"></a>

The following example creates a new ResourceShare\.

#### JSON<a name="aws-resource-ram-resourceshare-example1.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09T00:00:00.000Z",
  "Resources": {
    "myresourceshare": {
      "Type": "AWS::RAM::ResourceShare",
      "Properties": {
        "Name": "My Resource Share",
        "ResourceArns": [
          "arn:aws:ec2:us-east-1:123456789012:resource-type/12345678-1234-1234-1234-12345678"
        ],
        "Principals": [
          "210987654321"
        ],
        "Tags": [
          {
            "Key": "Key1",
            "Value": "Value1"
          },
          {
            "Key": "Key2",
            "Value": "Value2"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ram-resourceshare-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myresourceshare:
    Type: "AWS::RAM::ResourceShare"
    Properties:
      Name: "My Resource Share"
      ResourceArns:
        - "arn:aws:ec2:us-east-1:123456789012:resource-type/12345678-1234-1234-1234-12345678"
      Principals:
        - "210987654321"
      Tags:
        - Key: "Key1"
          Value: "Value1"
        - Key: "Key2"
          Value: "Value2"
```

## See Also<a name="aws-resource-ram-resourceshare-seealso"></a>
+  [CreateResourceShare](https://docs.aws.amazon.com/ram/latest/APIReference/API_CreateResourceShare.html) in the *AWS RAM API Reference* 