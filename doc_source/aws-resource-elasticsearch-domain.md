# AWS::Elasticsearch::Domain<a name="aws-resource-elasticsearch-domain"></a>

The `AWS::Elasticsearch::Domain` resource creates an Amazon Elasticsearch Service \(Amazon ES\) domain that encapsulates the Amazon ES engine instances\. For more information, see [CreateElasticsearchDomain](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) in the *Amazon Elasticsearch Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-elasticsearch-domain-syntax)
+ [Properties](#w3ab2c21c10d656b9)
+ [Return Values](#w3ab2c21c10d656c11)
+ [Examples](#aws-resource-elasticsearch-domain-examples)

## Syntax<a name="aws-resource-elasticsearch-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticsearch-domain-syntax.json"></a>

```
{
  "Type" : "AWS::Elasticsearch::Domain",
  "Properties" : {
    "[AccessPolicies](#cfn-elasticsearch-domain-accesspolicies)" : JSON object,
    "[AdvancedOptions](#cfn-elasticsearch-domain-advancedoptions)" : { String:String, ... },
    "[DomainName](#cfn-elasticsearch-domain-domainname)" : String,
    "[EBSOptions](#cfn-elasticsearch-domain-ebsoptions)" : [*EBSOptions*](aws-properties-elasticsearch-domain-ebsoptions.md),
    "[ElasticsearchClusterConfig](#cfn-elasticsearch-domain-elasticsearchclusterconfig)" : [*ElasticsearchClusterConfig*](aws-properties-elasticsearch-domain-elasticsearchclusterconfig.md),
    "[ElasticsearchVersion](#cfn-elasticsearch-domain-elasticsearchversion)" : String,
    "[EncryptionAtRestOptions](#cfn-elasticsearch-domain-encryptionatrestoptions)" : [*EncryptionAtRestOptions*](aws-properties-elasticsearch-domain-encryptionatrestoptions.md),
    "[SnapshotOptions](#cfn-elasticsearch-domain-snapshotoptions)" : [*SnapshotOptions*](aws-properties-elasticsearch-domain-snapshotoptions.md),
    "[Tags](#cfn-elasticsearch-domain-tags)" : [ Resource Tag, ... ],
    "[VPCOptions](#cfn-elasticsearch-domain-vpcoptions)" : [*VPCOptions*](aws-properties-elasticsearch-domain-vpcoptions.md)
  }
}
```

### YAML<a name="aws-resource-elasticsearch-domain-syntax.yaml"></a>

```
Type: "AWS::Elasticsearch::Domain"
Properties: 
  [AccessPolicies](#cfn-elasticsearch-domain-accesspolicies): JSON object
  [AdvancedOptions](#cfn-elasticsearch-domain-advancedoptions):
    String: String
  [DomainName](#cfn-elasticsearch-domain-domainname): String
  [EBSOptions](#cfn-elasticsearch-domain-ebsoptions):
    [*EBSOptions*](aws-properties-elasticsearch-domain-ebsoptions.md)
  [ElasticsearchClusterConfig](#cfn-elasticsearch-domain-elasticsearchclusterconfig):
    [*ElasticsearchClusterConfig*](aws-properties-elasticsearch-domain-elasticsearchclusterconfig.md)
  [ElasticsearchVersion](#cfn-elasticsearch-domain-elasticsearchversion): String
  [EncryptionAtRestOptions](#cfn-elasticsearch-domain-encryptionatrestoptions): 
    [*EncryptionAtRestOptions*](aws-properties-elasticsearch-domain-encryptionatrestoptions.md)
  [SnapshotOptions](#cfn-elasticsearch-domain-snapshotoptions):
    [*SnapshotOptions*](aws-properties-elasticsearch-domain-snapshotoptions.md)
  [Tags](#cfn-elasticsearch-domain-tags):
    - Resource Tag
  [VPCOptions](#cfn-elasticsearch-domain-vpcoptions): 
    [*VPCOptions*](aws-properties-elasticsearch-domain-vpcoptions.md)
```

## Properties<a name="w3ab2c21c10d656b9"></a>

`AccessPolicies`  <a name="cfn-elasticsearch-domain-accesspolicies"></a>
An AWS Identity and Access Management \(IAM\) policy document that specifies who can access the Amazon ES domain and their permissions\. For more information, see [Configuring Access Policies](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-access-policies) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AdvancedOptions`  <a name="cfn-elasticsearch-domain-advancedoptions"></a>
Additional options to specify for the Amazon ES domain\. For more information, see [Configuring Advanced Options](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-advanced-options) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: A JSON object that consists of a string key\-value pair, such as:  

```
{
  "rest.action.multi.allow_explicit_index": "true"
}
```
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DomainName`  <a name="cfn-elasticsearch-domain-domainname"></a>
A name for the Amazon ES domain\. For valid values, see the [DomainName](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-datatypes-domainname) data type in the *Amazon Elasticsearch Service Developer Guide*\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the domain name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EBSOptions`  <a name="cfn-elasticsearch-domain-ebsoptions"></a>
The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the Amazon ES domain\. For more information, see [Configuring EBS\-based Storage](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomain-configure-ebs) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: [Amazon ES Domain EBSOptions](aws-properties-elasticsearch-domain-ebsoptions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ElasticsearchClusterConfig`  <a name="cfn-elasticsearch-domain-elasticsearchclusterconfig"></a>
The cluster configuration for the Amazon ES domain\. You can specify options such as the instance type and the number of instances\. For more information, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: [Amazon ES Domain ElasticsearchClusterConfig](aws-properties-elasticsearch-domain-elasticsearchclusterconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ElasticsearchVersion`  <a name="cfn-elasticsearch-domain-elasticsearchversion"></a>
The version of Elasticsearch to use, such as `2.3`\. For information about the versions that Amazon ES supports, see the `Elasticsearch-Version` parameter for the [CreateElasticsearchDomain](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) action in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EncryptionAtRestOptions`  <a name="cfn-elasticsearch-domain-encryptionatrestoptions"></a>
Whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\. Can only be used to create a new domain, not update an existing one\.  
 *Required*: No  
 *Type*: [Amazon ES Domain EncryptionAtRestOptions](aws-properties-elasticsearch-domain-encryptionatrestoptions.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SnapshotOptions`  <a name="cfn-elasticsearch-domain-snapshotoptions"></a>
The automated snapshot configuration for the Amazon ES domain indices\.  
*Required*: No  
*Type*: [Amazon ES Domain SnapshotOptions](aws-properties-elasticsearch-domain-snapshotoptions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-elasticsearch-domain-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with the Amazon ES domain\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VPCOptions`  <a name="cfn-elasticsearch-domain-vpcoptions"></a>
The virtual private cloud \(VPC\) configuration for the Amazon ES domain\. For more information, see [VPC Support for Amazon Elasticsearch Service Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-vpc.html) in the *Amazon Elasticsearch Service Developer Guide*\.  
 *Required*: No  
 *Type*: [Amazon ES Domain VPCOptions](aws-properties-elasticsearch-domain-vpcoptions.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="w3ab2c21c10d656c11"></a>

### Ref<a name="w3ab2c21c10d656c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name, such as `mystack-elasticsea-abc1d2efg3h4`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d656c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the domain, such as `arn:aws:es:us-west-2:123456789012:domain/mystack-elasti-1ab2cdefghij`\.

`DomainArn` \(deprecated\)  
This attribute has been deprecated\. Use the `Arn` attribute instead\.

`DomainEndpoint`  
The domain\-specific endpoint that's used to submit index, search, and data upload requests to an Amazon ES domain, such as `search-mystack-elasti-1ab2cdefghij-ab1c2deckoyb3hofw7wpqa3cm.us-west-2.es.amazonaws.com`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-elasticsearch-domain-examples"></a>

### <a name="w3ab2c21c10d656c13b2"></a>

The following examples create an Amazon ES domain that contains two data nodes and three master nodes\. Automated snapshots of the indices are taken daily between midnight and 1:00 AM \(UTC\)\. The access policy permits the IAM user `es-user` to take all Amazon ES actions on the domain, such as `es:UpdateElasticsearchDomainConfig`\.

#### JSON<a name="aws-resource-elasticsearch-domain-example.json"></a>

```
"ElasticsearchDomain": {
  "Type": "AWS::Elasticsearch::Domain",
  "Properties": {
    "DomainName": "test",
    "ElasticsearchClusterConfig": {
      "DedicatedMasterEnabled": "true",
      "InstanceCount": "2",
      "ZoneAwarenessEnabled": "true",
      "InstanceType": "m3.medium.elasticsearch",
      "DedicatedMasterType": "m3.medium.elasticsearch",
      "DedicatedMasterCount": "3"
    },
    "EBSOptions": {
      "EBSEnabled": true,
      "Iops": 0,
      "VolumeSize": 20,
      "VolumeType": "gp2"
    },
    "SnapshotOptions": {
      "AutomatedSnapshotStartHour": "0"
    },
    "AccessPolicies": {
      "Version": "2012-10-17",
      "Statement": [{
        "Effect": "Allow",
        "Principal": {
          "AWS": "arn:aws:iam::123456789012:user/es-user"
        },
        "Action": "es:*",
        "Resource": "arn:aws:es:us-east-1:123456789012:domain/test/*"
      }]
    },
    "AdvancedOptions": {
      "rest.action.multi.allow_explicit_index": "true"
    }
  }
}
```

#### YAML<a name="aws-resource-elasticsearch-domain-example.yaml"></a>

```
ElasticsearchDomain: 
  Type: "AWS::Elasticsearch::Domain"
  Properties:
    DomainName: "test"
    ElasticsearchClusterConfig: 
      DedicatedMasterEnabled: "true"
      InstanceCount: "2"
      ZoneAwarenessEnabled: "true"
      InstanceType: "m3.medium.elasticsearch"
      DedicatedMasterType: "m3.medium.elasticsearch"
      DedicatedMasterCount: "3"
    EBSOptions: 
      EBSEnabled: true
      Iops: 0
      VolumeSize: 20
      VolumeType: "gp2"
    SnapshotOptions: 
      AutomatedSnapshotStartHour: "0"
    AccessPolicies: 
      Version: "2012-10-17"
      Statement: 
        - 
          Effect: "Allow"
          Principal: 
            AWS: "arn:aws:iam::123456789012:user/es-user"
          Action: "es:*"
          Resource: "arn:aws:es:us-east-1:846973539254:domain/test/*"
    AdvancedOptions: 
      rest.action.multi.allow_explicit_index: "true"
```

### <a name="aws-resource-elasticsearch-domain-example2"></a>

The following example creates a domain with VPC options\.

#### JSON<a name="aws-resource-elasticsearch-domain-example2.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "ElasticsearchDomain resource",
  "Parameters": {
    "DomainName" : {
      "Description" : "User defined Elasticsearch Domain name",
      "Type" : "String"
    },
    "ElasticsearchVersion" : {
      "Description" : "User defined Elasticsearch Version",
      "Type" : "String"
    },
    "InstanceType" : {
      "Type" : "String"
    },
    "AvailabilityZone" : {
      "Type" : "String"
    },
    "CidrBlock" : {
      "Type" : "String"
    },
    "GroupDescription" : {
      "Type" : "String"
    },
    "SGName" : {
      "Type" : "String"
    }
  },
  "Resources": {
    "ElasticsearchDomain": {
      "Type": "AWS::Elasticsearch::Domain",
      "Properties": {
        "DomainName": { "Ref": "DomainName" },
        "ElasticsearchVersion": { "Ref": "ElasticsearchVersion" },
        "ElasticsearchClusterConfig": {
          "InstanceCount": "1",
          "InstanceType": { "Ref": "InstanceType" }
        },
        "EBSOptions": {
          "EBSEnabled" : "true",
          "Iops" : 0,
          "VolumeSize" : 10,
          "VolumeType" : "standard"
        },
        "SnapshotOptions": {
          "AutomatedSnapshotStartHour": "0"
        },
        "AccessPolicies": {
          "Version": "2012-10-17",
          "Statement": [{
            "Effect": "Deny",
            "Principal": {
              "AWS": "*"
            },
            "Action": "es:*",
            "Resource": "*"
          }]
        },
        "AdvancedOptions": {
          "rest.action.multi.allow_explicit_index": "true"
        },
        "Tags": [{
          "Key": "foo",
          "Value": "bar"
        }],
        "VPCOptions" : {
          "SubnetIds" : [
            {"Ref" : "subnet"}
          ],
          "SecurityGroupIds" : [
            {"Ref" : "mySecurityGroup"}
          ]
        }
      }
    },
    "vpc" : {
      "Type" : "AWS::EC2::VPC",
      "Properties" : {
        "CidrBlock" : "10.0.0.0/16"
      }
    },
    "subnet" : {
      "Type" : "AWS::EC2::Subnet",
      "Properties" : {
        "VpcId" : {"Ref": "vpc"},
        "CidrBlock" : {"Ref" : "CidrBlock"},
        "AvailabilityZone" : {"Ref" : "AvailabilityZone"}
      }
    },
    "mySecurityGroup": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "GroupDescription": {"Ref" : "GroupDescription"},
        "VpcId" : {"Ref" : "vpc"},
        "GroupName": {"Ref" : "SGName"},
        "SecurityGroupIngress": [
          {
            "FromPort": "443",
            "IpProtocol": "tcp",
            "ToPort": "443",
            "CidrIp": "0.0.0.0/0"
          }
        ]
      }
    }
  },
  "Outputs": {
    "DomainArn": {
      "Value": {
        "Fn::GetAtt": ["ElasticsearchDomain", "DomainArn"]
      }
    },
    "DomainEndpoint": {
      "Value": {
        "Fn::GetAtt": ["ElasticsearchDomain", "DomainEndpoint"]
      }
    },
    "SecurityGroupId": {
      "Value": {
        "Ref": "mySecurityGroup"
      }
    },
    "SubnetId": {
      "Value": {
        "Ref": "subnet"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-elasticsearch-domain-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: ElasticsearchDomain resource
Parameters:
  DomainName:
    Description: User defined Elasticsearch Domain name
    Type: String
  ElasticsearchVersion:
    Description: User defined Elasticsearch Version
    Type: String
  InstanceType:
    Type: String
  AvailabilityZone:
    Type: String
  CidrBlock:
    Type: String
  GroupDescription:
    Type: String
  SGName:
    Type: String
Resources:
  ElasticsearchDomain:
    Type: 'AWS::Elasticsearch::Domain'
    Properties:
      DomainName: !Ref DomainName
      ElasticsearchVersion: !Ref ElasticsearchVersion
      ElasticsearchClusterConfig:
        InstanceCount: '1'
        InstanceType: !Ref InstanceType
      EBSOptions:
        EBSEnabled: 'true'
        Iops: 0
        VolumeSize: 10
        VolumeType: standard
      SnapshotOptions:
        AutomatedSnapshotStartHour: '0'
      AccessPolicies:
        Version: 2012-10-17
        Statement:
          - Effect: Deny
            Principal:
              AWS: '*'
            Action: 'es:*'
            Resource: '*'
      AdvancedOptions:
        rest.action.multi.allow_explicit_index: 'true'
      Tags:
        - Key: foo
          Value: bar
      VPCOptions:
        SubnetIds:
          - !Ref subnet
        SecurityGroupIds:
          - !Ref mySecurityGroup
  vpc:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
  subnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref vpc
      CidrBlock: !Ref CidrBlock
      AvailabilityZone: !Ref AvailabilityZone
  mySecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: !Ref GroupDescription
      VpcId: !Ref vpc
      GroupName: !Ref SGName
      SecurityGroupIngress:
        - FromPort: '443'
          IpProtocol: tcp
          ToPort: '443'
          CidrIp: 0.0.0.0/0
Outputs:
  DomainArn:
    Value: !GetAtt ElasticsearchDomain.DomainArn
  DomainEndpoint:
    Value: !GetAtt ElasticsearchDomain.DomainEndpoint
  SecurityGroupId:
    Value: !Ref mySecurityGroup
  SubnetId:
    Value: !Ref subnet
```