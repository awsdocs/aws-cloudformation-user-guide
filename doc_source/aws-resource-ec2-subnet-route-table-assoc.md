# AWS::EC2::SubnetRouteTableAssociation<a name="aws-resource-ec2-subnet-route-table-assoc"></a>

Associates a subnet with a route table\.

When `AWS::EC2::SubnetRouteTableAssociation` resources are created during create or update operations, AWS CloudFormation adopts existing resources that share the same key properties \(the properties that contribute to uniquely identify the resource\)\. However, if the operation fails and rolls back, AWS CloudFormation deletes the previously out\-of\-band resources\. You can protect against this behavior by using `Retain` deletion policies\. For more information, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

**Topics**
+ [Syntax](#aws-resource-ec2-subnetroutetableassociation-syntax)
+ [Properties](#w3ab2c21c10d498c11)
+ [Return Value](#w3ab2c21c10d498c13)
+ [Example](#w3ab2c21c10d498c15)
+ [See Also](#w3ab2c21c10d498c17)

## Syntax<a name="aws-resource-ec2-subnetroutetableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnetroutetableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SubnetRouteTableAssociation",
  "Properties" : {
    "[RouteTableId](#cfn-ec2-subnetroutetableassociation-routetableid)" : String,
    "[SubnetId](#cfn-ec2-subnetroutetableassociation-subnetid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-subnetroutetableassociation-syntax.yaml"></a>

```
Type: "AWS::EC2::SubnetRouteTableAssociation"
Properties: 
  [RouteTableId](#cfn-ec2-subnetroutetableassociation-routetableid): String
  [SubnetId](#cfn-ec2-subnetroutetableassociation-subnetid): String
```

## Properties<a name="w3ab2c21c10d498c11"></a>

`RouteTableId`  <a name="cfn-ec2-subnetroutetableassociation-routetableid"></a>
The ID of the route table\. This is commonly written as a reference to a route table declared elsewhere in the template\. For example:  

```
"RouteTableId" : { "Ref" : "myRouteTable" }
```
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. However, the physical ID changes when the route table ID is changed\.

`SubnetId`  <a name="cfn-ec2-subnetroutetableassociation-subnetid"></a>
The ID of the subnet\. This is commonly written as a reference to a subnet declared elsewhere in the template\. For example:  

```
"SubnetId" : { "Ref" : "mySubnet" }
```
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d498c13"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyRTA" }
```

For the subnet route table association with the logical ID "MyRTA", Ref will return the AWS resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d498c15"></a>

### JSON<a name="aws-resource-subnetroutetableassociation-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "mySubnetRouteTableAssociation" : {
         "Type" : "AWS::EC2::SubnetRouteTableAssociation",
         "Properties" : {
            "SubnetId" : { "Ref" : "mySubnet" },
            "RouteTableId" : { "Ref" : "myRouteTable" }
         }
      }
   }
}
```

### YAML<a name="aws-resource-subnetroutetableassociation-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  mySubnetRouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      SubnetId:
        Ref: mySubnet
      RouteTableId:
        Ref: myRouteTable
```

## See Also<a name="w3ab2c21c10d498c17"></a>
+ [AssociateRouteTable](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AssociateRouteTable.html) in the *Amazon EC2 API Reference*