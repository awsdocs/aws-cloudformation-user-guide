# AWS::EC2::RouteTable<a name="aws-resource-ec2-route-table"></a>

Creates a new route table within a VPC\. After you create a new route table, you can add routes and associate the table with a subnet\.

**Topics**
+ [Syntax](#aws-resource-ec2-routetable-syntax)
+ [Properties](#w3ab2c21c10d460b9)
+ [Return Values](#w3ab2c21c10d460c11)
+ [Examples](#w3ab2c21c10d460c13)
+ [See Also](#w3ab2c21c10d460c15)

## Syntax<a name="aws-resource-ec2-routetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-routetable-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::RouteTable",
   "Properties" : {
      "[VpcId](#cfn-ec2-routetable-vpcid)" : String,
      "[Tags](#cfn-ec2-routetable-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-routetable-syntax.yaml"></a>

```
Type: "AWS::EC2::RouteTable"
Properties: 
  [VpcId](#cfn-ec2-routetable-vpcid): String
  [Tags](#cfn-ec2-routetable-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d460b9"></a>

`VpcId`  <a name="cfn-ec2-routetable-vpcid"></a>
The ID of the VPC where the route table will be created\.  
Example: vpc\-11ad4878  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-routetable-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this route table\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

## Return Values<a name="w3ab2c21c10d460c11"></a>

### Ref<a name="w3ab2c21c10d460c11b2"></a>

When you specify an `AWS::EC2::RouteTable` type as an argument to the `Ref` function, AWS CloudFormation returns the route table ID, such as `rtb-12a34567`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d460c13"></a>

The following example snippet uses the VPC ID from a VPC named *myVPC* that was declared elsewhere in the same template\.

### JSON<a name="aws-resource-ec2-routetable-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myRouteTable" : {
         "Type" : "AWS::EC2::RouteTable",
         "Properties" : {
            "VpcId" : { "Ref" : "myVPC" },
            "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-routetable-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:
        Ref: myVPC
      Tags:
      - Key: foo
        Value: bar
```

## See Also<a name="w3ab2c21c10d460c15"></a>
+ [AWS::EC2::Route](aws-resource-ec2-route.md)
+ [CreateRouteTable](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateRouteTable.html) in the *Amazon EC2 API Reference*
+ [Route Tables](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*
+ [Using Tags](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*