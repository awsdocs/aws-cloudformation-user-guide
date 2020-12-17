# AWS::DAX::SubnetGroup<a name="aws-resource-dax-subnetgroup"></a>

Creates a new subnet group\.

## Syntax<a name="aws-resource-dax-subnetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dax-subnetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::DAX::SubnetGroup",
  "Properties" : {
      "[Description](#cfn-dax-subnetgroup-description)" : String,
      "[SubnetGroupName](#cfn-dax-subnetgroup-subnetgroupname)" : String,
      "[SubnetIds](#cfn-dax-subnetgroup-subnetids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-dax-subnetgroup-syntax.yaml"></a>

```
Type: AWS::DAX::SubnetGroup
Properties: 
  [Description](#cfn-dax-subnetgroup-description): String
  [SubnetGroupName](#cfn-dax-subnetgroup-subnetgroupname): String
  [SubnetIds](#cfn-dax-subnetgroup-subnetids): 
    - String
```

## Properties<a name="aws-resource-dax-subnetgroup-properties"></a>

`Description`  <a name="cfn-dax-subnetgroup-description"></a>
The description of the subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetGroupName`  <a name="cfn-dax-subnetgroup-subnetgroupname"></a>
The name of the subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-dax-subnetgroup-subnetids"></a>
A list of VPC subnet IDs for the subnet group\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dax-subnetgroup-return-values"></a>

### Ref<a name="aws-resource-dax-subnetgroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the created subnet group\. For example 

```
{ "Ref": "MyDAXSubnetGroup" }
```

Returns a value similar to the following:

```
my-dax-subnet-group
```

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-dax-subnetgroup--examples"></a>

### Create Subnet group<a name="aws-resource-dax-subnetgroup--examples--Create_Subnet_group"></a>

The following example creates a DAX subnet group\.

#### JSON<a name="aws-resource-dax-subnetgroup--examples--Create_Subnet_group--json"></a>

```
  {
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Create a DAX subnet group",
  "Resources": {
    "MyDAXSubnetGroup": {
      "Type": "AWS::DAX::SubnetGroup",
      "Properties": {
        "SubnetGroupName": "my-dax-subnet-group",
        "Description": "Description of my DAX subnet group",
        "SubnetIds": [
          "subnet1",
          "subnet2"
        ]
      }
    },
    "subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": "daxVPC",
        "CidrBlock": "172.13.17.0/24",
        "AvailabilityZone": {
          "Fn::Select": [
            0,
            {
              "Fn::GetAZs": ""
            }
          ]
        }
      }
    },
    "subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": "daxVPC",
        "CidrBlock": "172.13.18.0/24",
        "AvailabilityZone": {
          "Fn::Select": [
            1,
            {
              "Fn::GetAZs": ""
            }
          ]
        }
      }
    },
    "daxVpc": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "172.13.0.0/16"
      }
    }
  },
  "Outputs": {
    "ParameterGroup": {
      "Value": "MyDAXSubnetGroup"
    }
  }
}
```

#### YAML<a name="aws-resource-dax-subnetgroup--examples--Create_Subnet_group--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "DAX subnet group"
Resources:
  MyDAXSubnetGroup:
    Type: AWS::DAX::SubnetGroup
    Properties:
      SubnetGroupName: "my-dax-subnet-group" 
      Description: "Description of my DAX subnet group" 
      SubnetIds:
        - !Ref subnet1
        - !Ref subnet2
  subnet1:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        !Ref daxVpc
      CidrBlock: 172.13.17.0/24
      AvailabilityZone:
        Fn::Select:
          - 0
          - Fn::GetAZs: ""
  subnet2:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        !Ref daxVpc
      CidrBlock: 172.13.18.0/24
      AvailabilityZone:
        Fn::Select:
          - 1
          - Fn::GetAZs: ""
  daxVpc:
     Type: AWS::EC2::VPC
     Properties:
       CidrBlock: 172.13.0.0/16
Outputs:
  ParameterGroup:
Value: !Ref MyDAXSubnetGroup
```