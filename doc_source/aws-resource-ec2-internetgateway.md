# AWS::EC2::InternetGateway<a name="aws-resource-ec2-internetgateway"></a>

Allocates an internet gateway for use with a VPC\. After creating the Internet gateway, you then attach it to a VPC\.

## Syntax<a name="aws-resource-ec2-internetgateway-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-internetgateway-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::InternetGateway",
  "Properties" : {
      "[Tags](#cfn-ec2-internetgateway-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-internetgateway-syntax.yaml"></a>

```
Type: AWS::EC2::InternetGateway
Properties: 
  [Tags](#cfn-ec2-internetgateway-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-internetgateway-properties"></a>

`Tags`  <a name="cfn-ec2-internetgateway-tags"></a>
Any tags to assign to the internet gateway\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-internetgateway-return-values"></a>

### Ref<a name="aws-resource-ec2-internetgateway-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-internetgateway-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-internetgateway-return-values-fn--getatt-fn--getatt"></a>

`InternetGatewayId`  <a name="InternetGatewayId-fn::getatt"></a>
The ID of the internet gateway\.

## Examples<a name="aws-resource-ec2-internetgateway--examples"></a>

### Create an internet gateway<a name="aws-resource-ec2-internetgateway--examples--Create_an_internet_gateway"></a>

The following example creates an internet gateway and assigns it a tag\.

#### JSON<a name="aws-resource-ec2-internetgateway--examples--Create_an_internet_gateway--json"></a>

```
"Resources" : {
   "myInternetGateway" : {
      "Type" : "AWS::EC2::InternetGateway",
      "Properties" : {
        "Tags" : [ {"Key" : "stack", "Value" : "production"}]
      }
   }
}
```

#### YAML<a name="aws-resource-ec2-internetgateway--examples--Create_an_internet_gateway--yaml"></a>

```
  myInternetGateway:
    Type: AWS::EC2::InternetGateway
    Properties:
      Tags:
      - Key: stack
        Value: production
```

## See also<a name="aws-resource-ec2-internetgateway--seealso"></a>
+  [ CreateInternetGateway](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateInternetGateway.html) in the *Amazon EC2 API Reference*
+ [Internet gateways](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html) in the *Amazon VPC User Guide*
+ Use the [ AWS::EC2::VPCGatewayAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html) resource to associate an internet gateway with a VPC