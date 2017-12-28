# AWS::RDS::DBSubnetGroup<a name="aws-resource-rds-dbsubnet-group"></a>

The AWS::RDS::DBSubnetGroup type creates an RDS database subnet group\. Subnet groups must contain at least two subnets in two different Availability Zones in the same region\.


+ [Syntax](#aws-resource-rds-dbsubnetgroup-syntax)
+ [Properties](#aws-resource-rds-dbsubnet-group-prop)
+ [Return Value](#aws-resource-rds-dbsubnet-group-return-value)
+ [Example](#aws-resource-rds-dbsubnet-group-example)
+ [See Also](#aws-resource-rds-dbsubnet-group-see-also)

## Syntax<a name="aws-resource-rds-dbsubnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbsubnetgroup-syntax.json"></a>

```
{
   "Type" : "AWS::RDS::DBSubnetGroup",
   "Properties" : {
      "DBSubnetGroupDescription" : String,
      "SubnetIds" : [ String, ... ],
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbsubnetgroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-rds-dbsubnetgroup-syntax.yaml"></a>

```
Type: "AWS::RDS::DBSubnetGroup"
Properties: 
  DBSubnetGroupDescription: String
  SubnetIds:
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbsubnetgroup-tags):
    - Resource Tag
```

## Properties<a name="aws-resource-rds-dbsubnet-group-prop"></a>

`DBSubnetGroupDescription`  
The description for the DB Subnet Group\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`SubnetIds`  
The EC2 Subnet IDs for the DB Subnet Group\.  
*Required: *Yes  
*Type*: List of String values  
*Update requires*: No interruption

`Tags`  
The tags that you want to attach to the RDS database subnet group\.  
*Required: *No  
*Type*: A list of resource tags in key\-value format\.  
*Update requires*: No interruption

## Return Value<a name="aws-resource-rds-dbsubnet-group-return-value"></a>

### Ref<a name="aws-resource-rds-dbsubnet-group-return-value-ref"></a>

When you pass the logical ID of an `AWS::RDS::DBSubnetGroup` resource to the intrinsic `Ref` function, the function returns the name of the DB subnet group, such as `mystack-mydbsubnetgroup-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="aws-resource-rds-dbsubnet-group-example"></a>

### JSON<a name="aws-resource-rds-dbsubnetgroup-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBSubnetGroup" : {
         "Type" : "AWS::RDS::DBSubnetGroup",
         "Properties" : {
            "DBSubnetGroupDescription" : "description",
            "SubnetIds" : [ "subnet-7b5b4112", "subnet-7b5b4115" ],
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-rds-dbsubnetgroup-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBSubnetGroup: 
    Type: "AWS::RDS::DBSubnetGroup"
    Properties: 
      DBSubnetGroupDescription: "description"
      SubnetIds: 
        - "subnet-7b5b4112"
        - "subnet-7b5b4115"
      Tags: 
        - 
          Key: "String"
          Value: "String"
```

## See Also<a name="aws-resource-rds-dbsubnet-group-see-also"></a>

+ [CreateDBSubnetGroup](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBSubnetGroup.html) in the *Amazon Relational Database Service API Reference*

+ [ModifyDBSubnetGroup](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBSubnetGroup.html) in the *Amazon Relational Database Service API Reference*

+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)