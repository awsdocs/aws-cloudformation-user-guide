# AWS::EC2::InternetGateway<a name="aws-resource-ec2-internetgateway"></a>

Creates a new Internet gateway in your AWS account\. After creating the Internet gateway, you then attach it to a VPC\.

## Syntax<a name="aws-resource-ec2-internetgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-internetgateway-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::InternetGateway",
   "Properties" : {
      "[Tags](#cfn-ec2-internetgateway-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-internetgateway-syntax.yaml"></a>

```
Type: AWS::EC2::InternetGateway
Properties: 
  [Tags](#cfn-ec2-internetgateway-tags):
    - Resource Tag
```

## Properties<a name="w4ab1c21c10d102c54b7"></a>

`Tags`  <a name="cfn-ec2-internetgateway-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this resource\.  
*Required*: No  
*Type*: [Resource Tag](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w4ab1c21c10d102c54b9"></a>

### Ref<a name="w4ab1c21c10d102c54b9b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w4ab1c21c10d102c54c11"></a>

### JSON<a name="aws-resource-ec2-internetgateway-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myInternetGateway" : {
         "Type" : "AWS::EC2::InternetGateway",
         "Properties" : {
            "Tags" : [ {"Key" : "foo", "Value" : "bar"}]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-internetgateway-example.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myInternetGateway:
    Type: AWS::EC2::InternetGateway
    Properties:
      Tags:
      - Key: foo
        Value: bar
```

## Related Information<a name="w4ab1c21c10d102c54c13"></a>
+ [CreateInternetGateway](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateInternetGateway.html) in the *Amazon EC2 API Reference*\.
+ Use the [AWS::EC2::VPCGatewayAttachment](aws-resource-ec2-vpc-gateway-attachment.md) resource to associate an Internet gateway with a VPC\.