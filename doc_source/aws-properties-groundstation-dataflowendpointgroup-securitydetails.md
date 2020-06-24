# AWS::GroundStation::DataflowEndpointGroup SecurityDetails<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails"></a>

 Information about IAM roles, subnets, and security groups needed for this DataflowEndpointGroup\. 

## Syntax<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails-syntax.json"></a>

```
{
  "[RoleArn](#cfn-groundstation-dataflowendpointgroup-securitydetails-rolearn)" : String,
  "[SecurityGroupIds](#cfn-groundstation-dataflowendpointgroup-securitydetails-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-groundstation-dataflowendpointgroup-securitydetails-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails-syntax.yaml"></a>

```
  [RoleArn](#cfn-groundstation-dataflowendpointgroup-securitydetails-rolearn): String
  [SecurityGroupIds](#cfn-groundstation-dataflowendpointgroup-securitydetails-securitygroupids): 
    - String
  [SubnetIds](#cfn-groundstation-dataflowendpointgroup-securitydetails-subnetids): 
    - String
```

## Properties<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails-properties"></a>

`RoleArn`  <a name="cfn-groundstation-dataflowendpointgroup-securitydetails-rolearn"></a>
The ARN of a role which Ground Station has permission to assume, such as `arn:aws:iam::1234567890:role/DataDeliveryServiceRole`\.   
 Ground Station will assume this role and create an ENI in your VPC on the specified subnet upon creation of a dataflow endpoint group\. This ENI is used as the ingress/egress point for data streamed during a satellite contact\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-groundstation-dataflowendpointgroup-securitydetails-securitygroupids"></a>
The security group Ids of the security role, such as `sg-1234567890abcdef0`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-groundstation-dataflowendpointgroup-securitydetails-subnetids"></a>
The subnet Ids of the security details, such as `subnet-12345678`\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails--examples"></a>

### Create SecurityDetails<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails--examples--Create_SecurityDetails"></a>

The following example creates Ground Station `SecurityDetails`

#### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails--examples--Create_SecurityDetails--json"></a>

```
{
  "SecurityDetails": {
    "SubnetIds": [
      "subnet-6782e71e"
    ],
    "SecurityGroupIds": [
      "sg-6979fe18"
    ],
    "RoleArn": "arn:aws:iam::012345678910:role/groundstation-service-role-AWSServiceRoleForAmazonGroundStation-EXAMPLEBQ4PI"
  }
}
```

#### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-securitydetails--examples--Create_SecurityDetails--yaml"></a>

```
SecurityDetails:
  SubnetIds:
    - subnet-12345678
  SecurityGroupIds:
    - sg-87654321
  RoleArn: arn:aws:iam::012345678910:role/groundstation-service-role-AWSServiceRoleForAmazonGroundStation-EXAMPLEABCDE
```