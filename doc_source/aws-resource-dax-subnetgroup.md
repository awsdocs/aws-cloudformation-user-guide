# AWS::DAX::SubnetGroup<a name="aws-resource-dax-subnetgroup"></a>

Use the AWS CloudFormation `AWS::DAX::SubnetGroup` resource to create a subnet group for use with DAX \(DynamoDB Accelerator\)\.

For more information, see [http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_SubnetGroup.html](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_dax_SubnetGroup.html) in the *Amazon DynamoDB Developer Guide*\.

## Syntax<a name="aws-resource-dax-subnetgroup-syntax"></a>

### JSON<a name="aws-resource-dax-subnetgroup-syntax.json"></a>

```
{
   "Type": "AWS::DAX::SubnetGroup",
   "Properties": {
      "[SubnetGroupName](#cfn-dax-subnetgroup-name)": String,
      "[Description](#cfn-dax-subnetgroup-description)": String,
      "[SubnetIds](#cfn-dax-subnetgroup-name-values)": [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-dax-subnetgroup-syntax.yaml"></a>

```
Type: "AWS::DAX::SubnetGroup"
Properties:
      [SubnetGroupName](#cfn-dax-subnetgroup-name): String
      [Description](#cfn-dax-subnetgroup-description): String
      [SubnetIds](#cfn-dax-subnetgroup-name-values): [ String, ... ]
```

## Properties<a name="w3ab2c21c10d336b9"></a>

`SubnetGroupName`  <a name="cfn-dax-subnetgroup-name"></a>
The name of the subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-dax-subnetgroup-description"></a>
The description of the subnet group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetIds`  <a name="cfn-dax-subnetgroup-name-values"></a>
A list of subnets associated with the subnet group\.  
*Required*: No  
*Type*: List of String values;  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-dax-subnetgroup-returnvalues"></a>

### Ref<a name="w3ab2c21c10d336c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created activity\. For example:

```
{ "Ref": "MyDAXSubnetGroup" }
```

Returns a value similar to the following:

```
my-dax-subnet-group
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d336c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`SubnetGroupName`  
Returns the name of the subnet group\. For example:  

```
{ "Fn::GetAtt": ["MyDAXSubnetGroup", "SubnetGroupName"] }
```
Returns a value similar to the following:  

```
my-dax-subnet-group
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-dax-subnetgroup-examples"></a>

The following example creates a DAX subnet group\.

### JSON<a name="aws-resource-dax-subnetgroup-example.json"></a>

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

### YAML<a name="aws-resource-dax-subnetgroup-example.yaml"></a>

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