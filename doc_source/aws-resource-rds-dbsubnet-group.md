# AWS::RDS::DBSubnetGroup<a name="aws-resource-rds-dbsubnet-group"></a>

The `AWS::RDS::DBSubnetGroup` resource creates a database subnet group\. Subnet groups must contain at least two subnets in two different Availability Zones in the same region\. 

For more information, see [ Working with DB Subnet Groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.WorkingWithRDSInstanceinaVPC.html#USER_VPC.Subnets) in the *Amazon RDS User Guide*\.

## Syntax<a name="aws-resource-rds-dbsubnet-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbsubnet-group-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBSubnetGroup",
  "Properties" : {
      "[DBSubnetGroupDescription](#cfn-rds-dbsubnetgroup-dbsubnetgroupdescription)" : String,
      "[DBSubnetGroupName](#cfn-rds-dbsubnetgroup-dbsubnetgroupname)" : String,
      "[SubnetIds](#cfn-rds-dbsubnetgroup-subnetids)" : [ String, ... ],
      "[Tags](#cfn-rds-dbsubnetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbsubnet-group-syntax.yaml"></a>

```
Type: AWS::RDS::DBSubnetGroup
Properties: 
  [DBSubnetGroupDescription](#cfn-rds-dbsubnetgroup-dbsubnetgroupdescription): String
  [DBSubnetGroupName](#cfn-rds-dbsubnetgroup-dbsubnetgroupname): String
  [SubnetIds](#cfn-rds-dbsubnetgroup-subnetids): 
    - String
  [Tags](#cfn-rds-dbsubnetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rds-dbsubnet-group-properties"></a>

`DBSubnetGroupDescription`  <a name="cfn-rds-dbsubnetgroup-dbsubnetgroupdescription"></a>
The description for the DB Subnet Group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBSubnetGroupName`  <a name="cfn-rds-dbsubnetgroup-dbsubnetgroupname"></a>
The name for the DB Subnet Group\. This value is stored as a lowercase string\.  
Constraints: Must contain no more than 255 lowercase alphanumeric characters or hyphens\. Must not be "Default"\.  
Example: `mysubnetgroup`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-rds-dbsubnetgroup-subnetids"></a>
The EC2 Subnet IDs for the DB Subnet Group\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbsubnetgroup-tags"></a>
Tags to assign to the DB subnet group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rds-dbsubnet-group-return-values"></a>

### Ref<a name="aws-resource-rds-dbsubnet-group-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB subnet group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-dbsubnet-group--examples"></a>



### <a name="aws-resource-rds-dbsubnet-group--examples--"></a>

#### JSON<a name="aws-resource-rds-dbsubnet-group--examples----json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "myDBSubnetGroup": {
            "Type": "AWS::RDS::DBSubnetGroup",
            "Properties": {
                "DBSubnetGroupDescription": "description",
                "SubnetIds": [
                    "subnet-7b5b4112",
                    "subnet-7b5b4115"
                ],
                "Tags": [
                    {
                        "Key": "String",
                        "Value": "String"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbsubnet-group--examples----yaml"></a>

```
--- 
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDBSubnetGroup: 
    Properties: 
      DBSubnetGroupDescription: description
      SubnetIds: 
        - subnet-7b5b4112
        - subnet-7b5b4115
      Tags: 
        - 
          Key: String
          Value: String
    Type: "AWS::RDS::DBSubnetGroup"
```