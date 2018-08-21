# AWS::Neptune::DBSubnetGroup<a name="aws-resource-neptune-dbsubnetgroup"></a>

The AWS::Neptune::DBSubnetGroup type creates a Neptune DB subnet group\. Subnet groups must contain at least two subnets in two different Availability Zones in the same region\.

**Topics**
+ [Syntax](#aws-resource-neptune-dbsubnetgroup-syntax)
+ [Properties](#aws-resource-neptune-dbsubnetgroup-prop)
+ [Return Value](#aws-resource-neptune-dbsubnetgroup-return-value)
+ [Example](#aws-resource-neptune-dbsubnetgroup-example)
+ [See Also](#aws-resource-neptune-dbsubnetgroup-see-also)

## Syntax<a name="aws-resource-neptune-dbsubnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbsubnetgroup-syntax.json"></a>

```
{
   "Type" : "AWS::Neptune::DBSubnetGroup",
   "Properties" : {
      "[DBSubnetGroupDescription](#cfn-neptune-dbsubnetgroup-dbsubnetgroupdescription)" : String,
      "[DBSubnetGroupName](#cfn-neptune-dbsubnetgroup-dbsubnetgroupname)" : String,
      "[SubnetIds](#cfn-neptune-dbsubnetgroup-subnetids)" : [ String, ... ],
      "[Tags](#cfn-neptune-dbsubnetgroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-neptune-dbsubnetgroup-syntax.yaml"></a>

```
Type: "AWS::Neptune::DBSubnetGroup"
Properties: 
  [DBSubnetGroupDescription](#cfn-neptune-dbsubnetgroup-dbsubnetgroupdescription): String
  [DBSubnetGroupName](#cfn-neptune-dbsubnetgroup-dbsubnetgroupname): String
  [SubnetIds](#cfn-neptune-dbsubnetgroup-subnetids):
    - String
  [Tags](#cfn-neptune-dbsubnetgroup-tags):
    - Resource Tag
```

## Properties<a name="aws-resource-neptune-dbsubnetgroup-prop"></a>

`DBSubnetGroupDescription`  <a name="cfn-neptune-dbsubnetgroup-dbsubnetgroupdescription"></a>
The description for the DB Subnet Group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-neptune-dbsubnetgroup-dbsubnetgroupname"></a>
The name for the DB Subnet Group\. This value is stored as a lowercase string\.  
Constraints: Must contain no more than 255 letters, numbers, periods, underscores, spaces, or hyphens\. Must not be default\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetIds`  <a name="cfn-neptune-dbsubnetgroup-subnetids"></a>
The EC2 Subnet IDs for the DB Subnet Group\.  
*Required*: Yes  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-neptune-dbsubnetgroup-tags"></a>
The tags that you want to attach to the RDS database subnet group\.  
*Required*: No  
*Type*: A list of [resource tags](aws-properties-resource-tags.md) in key\-value format\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-neptune-dbsubnetgroup-return-value"></a>

### Ref<a name="aws-resource-neptune-dbsubnetgroup-return-value-ref"></a>

When you pass the logical ID of an `AWS::Neptune::DBSubnetGroup` resource to the intrinsic `Ref` function, the function returns the name of the DB subnet group, such as `mystack-mydbsubnetgroup-0a12bc456789de0fg`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-neptune-dbsubnetgroup-example"></a>

### JSON<a name="aws-resource-neptune-dbsubnetgroup-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myDBSubnetGroup" : {
         "Type" : "AWS::Neptune::DBSubnetGroup",
         "Properties" : {
            "DBSubnetGroupDescription" : "description",
            "SubnetIds" : [ "subnet-7b5b4112", "subnet-7b5b4115" ],
            "Tags" : [ {"Key" : "String", "Value" : "String"} ]
         }
      }
   }
}
```

### YAML<a name="aws-resource-neptune-dbsubnetgroup-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBSubnetGroup: 
    Type: "AWS::Neptune::DBSubnetGroup"
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

## See Also<a name="aws-resource-neptune-dbsubnetgroup-see-also"></a>
+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)