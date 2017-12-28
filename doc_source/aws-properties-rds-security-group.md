# AWS::RDS::DBSecurityGroup<a name="aws-properties-rds-security-group"></a>

The AWS::RDS::DBSecurityGroup type is used to create or update an Amazon RDS DB Security Group\. For more information about DB security groups, see [Working with DB Security Groups](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithSecurityGroups.html) in the *Amazon Relational Database Service Developer Guide*\. For details on the settings for DB security groups, see [CreateDBSecurityGroup](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBSecurityGroup.html)\.

**Note**  
If you use DB security groups, the settings that you can specify for your DB instances are limited\. For more information, see the DBSecurityGroups property\.

When you specify an AWS::RDS::DBSecurityGroup as an argument to the `Ref` function, AWS CloudFormation returns the value of the `DBSecurityGroupName`\.


+ [Syntax](#aws-resource-rds-securitygroup-syntax)
+ [Properties](#w3ab2c21c10d895c13)
+ [Template Examples](#w3ab2c21c10d895c15)

## Syntax<a name="aws-resource-rds-securitygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-securitygroup-syntax.json"></a>

```
{
   "Type" : "AWS::RDS::DBSecurityGroup",
   "Properties" :
   {
      "EC2VpcId" : { "Ref" : "myVPC" },
      "DBSecurityGroupIngress" : [ RDS Security Group Rule object 1, ... ],
      "GroupDescription" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbsecuritygroup-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-rds-securitygroup-syntax.yaml"></a>

```
Type: "AWS::RDS::DBSecurityGroup"
Properties:
  EC2VpcId: String
  DBSecurityGroupIngress:
    - RDS Security Group Rule
  GroupDescription: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-rds-dbsecuritygroup-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10d895c13"></a>

`EC2VpcId`  
The Id of the VPC\. Indicates which VPC this DB Security Group should belong to\.  
The `EC2VpcId` property exists only for backwards compatibility with older regions and is no longer recommended for providing security information to an RDS DB instance\. Instead, use `VPCSecurityGroups`\.
*Type*: String  
*Required*: Conditional\. Must be specified to create a DB Security Group for a VPC; may not be specified otherwise\.   
*Update requires*: Replacement

`DBSecurityGroupIngress`  
Network ingress authorization for an Amazon EC2 security group or an IP address range\.  
*Type*: List of RDS Security Group Rules\.  
*Required*: Yes  
*Update requires*: No interruption

`GroupDescription`  
Description of the security group\.  
*Type*: String  
*Required*: Yes  
*Update requires*: Replacement

`Tags`  
The tags that you want to attach to the Amazon RDS DB security group\.  
*Required: *No  
*Type*: A list of resource tags\.  
*Update requires*: No interruption

## Template Examples<a name="w3ab2c21c10d895c15"></a>

**Tip**  
For more RDS template examples, see \.

### Single VPC security group<a name="w3ab2c21c10d895c15b4"></a>

This template snippet creates/updates a single VPC security group, referred to by EC2SecurityGroupName\.

#### JSON<a name="aws-resource-rds-securitygroup-example1.json"></a>

```
"DBSecurityGroup": {
   "Type": "AWS::RDS::DBSecurityGroup",
   "Properties": {
      "EC2VpcId" : { "Ref" : "VpcId" },
      "DBSecurityGroupIngress": [
         {"EC2SecurityGroupName": { "Ref": "WebServerSecurityGroup"}}
      ],
      "GroupDescription": "Frontend Access"
   }
}
```

#### YAML<a name="aws-resource-rds-securitygroup-example1.yaml"></a>

```
DBSecurityGroup: 
  Type: "AWS::RDS::DBSecurityGroup"
  Properties: 
    EC2VpcId: 
      Ref: "VpcId"
    DBSecurityGroupIngress: 
      - 
        EC2SecurityGroupName: 
          Ref: "WebServerSecurityGroup"
    GroupDescription: "Frontend Access"
```

### Multiple VPC security groups<a name="w3ab2c21c10d895c15b6"></a>

This template snippet creates/updates multiple VPC security groups\.

#### JSON<a name="aws-resource-rds-securitygroup-example2.json"></a>

```
{
   "Resources" : {
      "DBinstance" : {
         "Type" : "AWS::RDS::DBInstance",
         "Properties" : {
            "DBSecurityGroups" : [ {"Ref" : "DbSecurityByEC2SecurityGroup"} ],
            "AllocatedStorage" : "5",
            "DBInstanceClass" : "db.m1.small",
            "Engine" : "MySQL",
            "MasterUsername" : "YourName",
            "MasterUserPassword" : "YourPassword"
         },
         "DeletionPolicy" : "Snapshot"
      },
      "DbSecurityByEC2SecurityGroup" : {
         "Type" : "AWS::RDS::DBSecurityGroup",
         "Properties" : {
            "GroupDescription" : "Ingress for Amazon EC2 security group",
            "DBSecurityGroupIngress" : [ {
                  "EC2SecurityGroupId" : "sg-b0ff1111",
                  "EC2SecurityGroupOwnerId" : "111122223333"
               }, {
                  "EC2SecurityGroupId" : "sg-ffd722222",
                  "EC2SecurityGroupOwnerId" : "111122223333"
               } ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-rds-securitygroup-example2.yaml"></a>

```
Resources: 
  DBinstance: 
    Type: "AWS::RDS::DBInstance"
    Properties: 
      DBSecurityGroups: 
        - 
          Ref: "DbSecurityByEC2SecurityGroup"
      AllocatedStorage: "5"
      DBInstanceClass: "db.m1.small"
      Engine: "MySQL"
      MasterUsername: "YourName"
      MasterUserPassword: "YourPassword"
    DeletionPolicy: "Snapshot"
  DbSecurityByEC2SecurityGroup: 
    Type: "AWS::RDS::DBSecurityGroup"
    Properties: 
      GroupDescription: "Ingress for Amazon EC2 security group"
      DBSecurityGroupIngress: 
        - 
          EC2SecurityGroupId: "sg-b0ff1111"
          EC2SecurityGroupOwnerId: "111122223333"
        - 
          EC2SecurityGroupId: "sg-ffd722222"
          EC2SecurityGroupOwnerId: "111122223333"
```