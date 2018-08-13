# Amazon RDS Template Snippets<a name="quickref-rds"></a>

**Topics**
+ [Amazon RDS DB Instance Resource](#scenario-rds-instance)
+ [Amazon RDS Oracle Database DB Instance Resource](#scenario-rds-oracleinstance)
+ [Amazon RDS DBSecurityGroup Resource for CIDR Range](#scenario-rds-security-group-cidr)
+ [Amazon RDS DBSecurityGroup with an Amazon EC2 security group](#scenario-rds-security-group-ec2)
+ [Multiple VPC security groups](#scenario-multiple-vpc-security-groups)
+ [Amazon RDS Database Instance in a VPC Security Group](#w3ab2c17c24c77c15)

## Amazon RDS DB Instance Resource<a name="scenario-rds-instance"></a>

This example shows an Amazon RDS DB Instance resource\. Because the optional EngineVersion property is not specified, the default engine version is used for this DB Instance\. For details about the default engine version and other default settings, see [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html)\. The DBSecurityGroups property authorizes network ingress to the AWS::RDS::DBSecurityGroup resources named MyDbSecurityByEC2SecurityGroup and MyDbSecurityByCIDRIPGroup\. For details, see [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\. The DB Instance resource also has a DeletionPolicy attribute set to Snapshot\. With the Snapshot DeletionPolicy set, AWS CloudFormation will take a snapshot of this DB Instance before deleting it during stack deletion\.

### JSON<a name="quickref-rds-example-1.json"></a>

```
 1. "MyDB" : {
 2.  "Type" : "AWS::RDS::DBInstance",
 3.  "Properties" : {
 4.      "DBSecurityGroups" : [
 5.         {"Ref" : "MyDbSecurityByEC2SecurityGroup"}, {"Ref" : "MyDbSecurityByCIDRIPGroup"} ],
 6.      "AllocatedStorage" : "5",
 7.      "DBInstanceClass" : "db.m1.small",
 8.      "Engine" : "MySQL",
 9.      "MasterUsername" : "MyName",
10.      "MasterUserPassword" : "MyPassword"
11.  },
12.  "DeletionPolicy" : "Snapshot"
13. }
```

### YAML<a name="quickref-rds-example-1.yaml"></a>

```
 1. MyDB:
 2.   Type: AWS::RDS::DBInstance
 3.   Properties:
 4.     DBSecurityGroups:
 5.     - Ref: MyDbSecurityByEC2SecurityGroup
 6.     - Ref: MyDbSecurityByCIDRIPGroup
 7.     AllocatedStorage: '5'
 8.     DBInstanceClass: db.m1.small
 9.     Engine: MySQL
10.     MasterUsername: MyName
11.     MasterUserPassword: MyPassword
12.   DeletionPolicy: Snapshot
```

## Amazon RDS Oracle Database DB Instance Resource<a name="scenario-rds-oracleinstance"></a>

This example creates an Oracle Database DB Instance resource by specifying the Engine as oracle\-ee with a license model of bring\-your\-own\-license\. For details about the settings for Oracle Database DB instances, see [CreateDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_CreateDBInstance.html)\. The DBSecurityGroups property authorizes network ingress to the AWS::RDS::DBSecurityGroup resources named MyDbSecurityByEC2SecurityGroup and MyDbSecurityByCIDRIPGroup\. For details, see [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\. The DB Instance resource also has a DeletionPolicy attribute set to Snapshot\. With the Snapshot DeletionPolicy set, AWS CloudFormation will take a snapshot of this DB Instance before deleting it during stack deletion\.

### JSON<a name="quickref-rds-example-2.json"></a>

```
 1. "MyDB" : {
 2.  "Type" : "AWS::RDS::DBInstance",
 3.  "Properties" : {
 4.      "DBSecurityGroups" : [
 5.         {"Ref" : "MyDbSecurityByEC2SecurityGroup"}, {"Ref" : "MyDbSecurityByCIDRIPGroup"} ],
 6.      "AllocatedStorage" : "5",
 7.      "DBInstanceClass" : "db.m1.small",
 8.      "Engine" : "oracle-ee",
 9.      "LicenseModel" : "bring-your-own-license",
10.      "MasterUsername" : "master",
11.      "MasterUserPassword" : "SecretPassword01"
12.  },
13.  "DeletionPolicy" : "Snapshot"
14. }
```

### YAML<a name="quickref-rds-example-2.yaml"></a>

```
 1. MyDB:
 2.   Type: AWS::RDS::DBInstance
 3.   Properties:
 4.     DBSecurityGroups:
 5.     - Ref: MyDbSecurityByEC2SecurityGroup
 6.     - Ref: MyDbSecurityByCIDRIPGroup
 7.     AllocatedStorage: '5'
 8.     DBInstanceClass: db.m1.small
 9.     Engine: oracle-ee
10.     LicenseModel: bring-your-own-license
11.     MasterUsername: master
12.     MasterUserPassword: SecretPassword01
13.   DeletionPolicy: Snapshot
```

## Amazon RDS DBSecurityGroup Resource for CIDR Range<a name="scenario-rds-security-group-cidr"></a>

This example shows an Amazon RDS DBSecurityGroup resource with ingress authorization for the specified CIDR range in the format ddd\.ddd\.ddd\.ddd/dd\. For details, see [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) and [Amazon RDS Security Group Rule](aws-properties-rds-security-group-rule.md)\.

### JSON<a name="quickref-rds-example-3.json"></a>

```
1. "MyDbSecurityByCIDRIPGroup" : {
2.  "Type" : "AWS::RDS::DBSecurityGroup",
3.  "Properties" : {
4.      "GroupDescription" : "Ingress for CIDRIP",
5.      "DBSecurityGroupIngress" : {
6.          "CIDRIP" : "192.168.0.0/32"
7.      }
8.  }
9. }
```

### YAML<a name="quickref-rds-example-3.yaml"></a>

```
1. MyDbSecurityByCIDRIPGroup:
2.   Type: AWS::RDS::DBSecurityGroup
3.   Properties:
4.     GroupDescription: Ingress for CIDRIP
5.     DBSecurityGroupIngress:
6.       CIDRIP: "192.168.0.0/32"
```

## Amazon RDS DBSecurityGroup with an Amazon EC2 security group<a name="scenario-rds-security-group-ec2"></a>

This example shows an [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) resource with ingress authorization from an Amazon EC2 security group referenced by MyEc2SecurityGroup\.

To do this, you define an EC2 security group and then use the intrinsic Ref function to refer to the EC2 security group within your DBSecurityGroup\.

### JSON<a name="quickref-rds-example-4.json"></a>

```
"DBInstance" : {
   "Type": "AWS::RDS::DBInstance",
   "Properties": {
      "DBName"            : { "Ref" : "DBName" },
      "Engine"            : "MySQL",
      "MasterUsername"    : { "Ref" : "DBUsername" },
      "DBInstanceClass"   : { "Ref" : "DBClass" },
      "DBSecurityGroups"  : [ { "Ref" : "DBSecurityGroup" } ],
      "AllocatedStorage"  : { "Ref" : "DBAllocatedStorage" },
      "MasterUserPassword": { "Ref" : "DBPassword" }
   }
},

"DBSecurityGroup": {
   "Type": "AWS::RDS::DBSecurityGroup",
   "Properties": {
      "DBSecurityGroupIngress": { "EC2SecurityGroupName": { "Ref": "WebServerSecurityGroup" } },
      "GroupDescription"      : "Frontend Access"
   }
},

"WebServerSecurityGroup" : {
   "Type" : "AWS::EC2::SecurityGroup",
   "Properties" : {
      "GroupDescription" : "Enable HTTP access via port 80 and SSH access",
      "SecurityGroupIngress" : [
         {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "CidrIp" : "0.0.0.0/0"},
         {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : "0.0.0.0/0"}
      ]
   }
}
```

### YAML<a name="quickref-rds-example-4.yaml"></a>

This example is extracted from the following full example: [Drupal\_Single\_Instance\_With\_RDS\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Drupal_Single_Instance_With_RDS.template)

```
DBInstance:
  Type: AWS::RDS::DBInstance
  Properties:
    DBName:
      Ref: DBName
    Engine: MySQL
    MasterUsername:
      Ref: DBUsername
    DBInstanceClass:
      Ref: DBClass
    DBSecurityGroups:
    - Ref: DBSecurityGroup
    AllocatedStorage:
      Ref: DBAllocatedStorage
    MasterUserPassword:
      Ref: DBPassword
DBSecurityGroup:
  Type: AWS::RDS::DBSecurityGroup
  Properties:
    DBSecurityGroupIngress:
      EC2SecurityGroupName:
        Ref: WebServerSecurityGroup
    GroupDescription: Frontend Access
WebServerSecurityGroup:
  Type: AWS::EC2::SecurityGroup
  Properties:
    GroupDescription: Enable HTTP access via port 80 and SSH access
    SecurityGroupIngress:
    - IpProtocol: tcp
      FromPort: '80'
      ToPort: '80'
      CidrIp: 0.0.0.0/0
    - IpProtocol: tcp
      FromPort: '22'
      ToPort: '22'
      CidrIp: 0.0.0.0/0
```

## Multiple VPC security groups<a name="scenario-multiple-vpc-security-groups"></a>

This example shows an [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md) resource with ingress authorization for multiple Amazon EC2 VPC security groups in [AWS::RDS::DBSecurityGroupIngress](aws-resource-rds-security-group-ingress.md)\.

### JSON<a name="quickref-rds-example-5.json"></a>

```
{
   "Resources" : {
      "DBinstance" : {
         "Type" : "AWS::RDS::DBInstance",
         "Properties" : {
            "AllocatedStorage" : "5",
            "DBInstanceClass" : "db.m1.small",
           "DBName" : {"Ref": "MyDBName" },
            "DBSecurityGroups" : [ { "Ref" : "DbSecurityByEC2SecurityGroup" } ],
            "DBSubnetGroupName" : { "Ref" : "MyDBSubnetGroup" },
            "Engine" : "MySQL",
           "MasterUserPassword": { "Ref" : "MyDBPassword" },
           "MasterUsername"    : { "Ref" : "MyDBUsername" }
        },
         "DeletionPolicy" : "Snapshot"
      },
      "DbSecurityByEC2SecurityGroup" : {
         "Type" : "AWS::RDS::DBSecurityGroup",
         "Properties" : {
            "GroupDescription" : "Ingress for Amazon EC2 security group",
           "EC2VpcId" : { "Ref" : "MyVPC" },
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

### YAML<a name="quickref-rds-example-5.yaml"></a>

```
Resources:
  DBinstance:
    Type: AWS::RDS::DBInstance
    Properties:
      AllocatedStorage: '5'
      DBInstanceClass: db.m1.small
      DBName:
        Ref: MyDBName
      DBSecurityGroups:
      - Ref: DbSecurityByEC2SecurityGroup
      DBSubnetGroupName:
        Ref: MyDBSubnetGroup
      Engine: MySQL
      MasterUserPassword:
        Ref: MyDBPassword
      MasterUsername:
        Ref: MyDBUsername
    DeletionPolicy: Snapshot
  DbSecurityByEC2SecurityGroup:
    Type: AWS::RDS::DBSecurityGroup
    Properties:
      GroupDescription: Ingress for Amazon EC2 security group
      EC2VpcId:
        Ref: MyVPC
      DBSecurityGroupIngress:
      - EC2SecurityGroupId: sg-b0ff1111
        EC2SecurityGroupOwnerId: '111122223333'
      - EC2SecurityGroupId: sg-ffd722222
        EC2SecurityGroupOwnerId: '111122223333'
```

## Amazon RDS Database Instance in a VPC Security Group<a name="w3ab2c17c24c77c15"></a>

This example shows an Amazon RDS database instance associated with an Amazon EC2 VPC security group\.

### JSON<a name="quickref-rds-example-6.json"></a>

```
{
  "DBEC2SecurityGroup": {
    "Type": "AWS::EC2::SecurityGroup",
    "Properties" : {
      "GroupDescription": "Open database for access",
      "SecurityGroupIngress" : [{
        "IpProtocol" : "tcp",
        "FromPort" : "3306",
        "ToPort" : "3306",
        "SourceSecurityGroupName" : { "Ref" : "WebServerSecurityGroup" }
      }]
    }
  },
  "DBInstance" : {
    "Type": "AWS::RDS::DBInstance",
    "Properties": {
      "DBName"            : { "Ref" : "DBName" },
      "Engine"            : "MySQL",
      "MultiAZ"           : { "Ref": "MultiAZDatabase" },
      "MasterUsername"    : { "Ref" : "DBUser" },
      "DBInstanceClass"   : { "Ref" : "DBClass" },
      "AllocatedStorage"  : { "Ref" : "DBAllocatedStorage" },
      "MasterUserPassword": { "Ref" : "DBPassword" },
      "VPCSecurityGroups" : [ { "Fn::GetAtt": [ "DBEC2SecurityGroup", "GroupId" ] } ]
    }
  }
}
```

### YAML<a name="quickref-rds-example-6.yaml"></a>

```
DBEC2SecurityGroup:
  Type: AWS::EC2::SecurityGroup
  Properties:
    GroupDescription: Open database for access
    SecurityGroupIngress:
    - IpProtocol: tcp
      FromPort: '3306'
      ToPort: '3306'
      SourceSecurityGroupName:
        Ref: WebServerSecurityGroup
DBInstance:
  Type: AWS::RDS::DBInstance
  Properties:
    DBName:
      Ref: DBName
    Engine: MySQL
    MultiAZ:
      Ref: MultiAZDatabase
    MasterUsername:
      Ref: DBUser
    DBInstanceClass:
      Ref: DBClass
    AllocatedStorage:
      Ref: DBAllocatedStorage
    MasterUserPassword:
      Ref: DBPassword
    VPCSecurityGroups:
    - !GetAtt DBEC2SecurityGroup.GroupId
```