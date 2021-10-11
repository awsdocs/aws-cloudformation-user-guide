# AWS::OpenSearchService::Domain<a name="aws-resource-opensearchservice-domain"></a>

The AWS::OpenSearchService::Domain resource creates an Amazon OpenSearch Service domain\.

## Syntax<a name="aws-resource-opensearchservice-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchservice-domain-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchService::Domain",
  "Properties" : {
      "[AccessPolicies](#cfn-opensearchservice-domain-accesspolicies)" : Json,
      "[AdvancedOptions](#cfn-opensearchservice-domain-advancedoptions)" : {Key : Value, ...},
      "[AdvancedSecurityOptions](#cfn-opensearchservice-domain-advancedsecurityoptions)" : AdvancedSecurityOptionsInput,
      "[ClusterConfig](#cfn-opensearchservice-domain-clusterconfig)" : ClusterConfig,
      "[CognitoOptions](#cfn-opensearchservice-domain-cognitooptions)" : CognitoOptions,
      "[DomainEndpointOptions](#cfn-opensearchservice-domain-domainendpointoptions)" : DomainEndpointOptions,
      "[DomainName](#cfn-opensearchservice-domain-domainname)" : String,
      "[EBSOptions](#cfn-opensearchservice-domain-ebsoptions)" : EBSOptions,
      "[EncryptionAtRestOptions](#cfn-opensearchservice-domain-encryptionatrestoptions)" : EncryptionAtRestOptions,
      "[EngineVersion](#cfn-opensearchservice-domain-engineversion)" : String,
      "[LogPublishingOptions](#cfn-opensearchservice-domain-logpublishingoptions)" : {Key : Value, ...},
      "[NodeToNodeEncryptionOptions](#cfn-opensearchservice-domain-nodetonodeencryptionoptions)" : NodeToNodeEncryptionOptions,
      "[SnapshotOptions](#cfn-opensearchservice-domain-snapshotoptions)" : SnapshotOptions,
      "[Tags](#cfn-opensearchservice-domain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VPCOptions](#cfn-opensearchservice-domain-vpcoptions)" : VPCOptions
    }
}
```

### YAML<a name="aws-resource-opensearchservice-domain-syntax.yaml"></a>

```
Type: AWS::OpenSearchService::Domain
Properties: 
  [AccessPolicies](#cfn-opensearchservice-domain-accesspolicies): Json
  [AdvancedOptions](#cfn-opensearchservice-domain-advancedoptions): 
    Key : Value
  [AdvancedSecurityOptions](#cfn-opensearchservice-domain-advancedsecurityoptions): 
    AdvancedSecurityOptionsInput
  [ClusterConfig](#cfn-opensearchservice-domain-clusterconfig): 
    ClusterConfig
  [CognitoOptions](#cfn-opensearchservice-domain-cognitooptions): 
    CognitoOptions
  [DomainEndpointOptions](#cfn-opensearchservice-domain-domainendpointoptions): 
    DomainEndpointOptions
  [DomainName](#cfn-opensearchservice-domain-domainname): String
  [EBSOptions](#cfn-opensearchservice-domain-ebsoptions): 
    EBSOptions
  [EncryptionAtRestOptions](#cfn-opensearchservice-domain-encryptionatrestoptions): 
    EncryptionAtRestOptions
  [EngineVersion](#cfn-opensearchservice-domain-engineversion): String
  [LogPublishingOptions](#cfn-opensearchservice-domain-logpublishingoptions): 
    Key : Value
  [NodeToNodeEncryptionOptions](#cfn-opensearchservice-domain-nodetonodeencryptionoptions): 
    NodeToNodeEncryptionOptions
  [SnapshotOptions](#cfn-opensearchservice-domain-snapshotoptions): 
    SnapshotOptions
  [Tags](#cfn-opensearchservice-domain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VPCOptions](#cfn-opensearchservice-domain-vpcoptions): 
    VPCOptions
```

## Properties<a name="aws-resource-opensearchservice-domain-properties"></a>

`AccessPolicies`  <a name="cfn-opensearchservice-domain-accesspolicies"></a>
An AWS Identity and Access Management \(IAM\) policy document that specifies who can access the OpenSearch Service domain and their permissions\. For more information, see [Configuring access policies](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ac.html#ac-creating) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedOptions`  <a name="cfn-opensearchservice-domain-advancedoptions"></a>
Additional options to specify for the OpenSearch Service domain\. For more information, see [Advanced cluster parameters](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html#createdomain-configure-advanced-options) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdvancedSecurityOptions`  <a name="cfn-opensearchservice-domain-advancedsecurityoptions"></a>
Specifies options for fine\-grained access control\.  
*Required*: No  
*Type*: [AdvancedSecurityOptionsInput](aws-properties-opensearchservice-domain-advancedsecurityoptionsinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterConfig`  <a name="cfn-opensearchservice-domain-clusterconfig"></a>
`ClusterConfig` is a property of the AWS::OpenSearchService::Domain resource that configures an Amazon OpenSearch Service cluster\.  
*Required*: No  
*Type*: [ClusterConfig](aws-properties-opensearchservice-domain-clusterconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CognitoOptions`  <a name="cfn-opensearchservice-domain-cognitooptions"></a>
Configures OpenSearch Service to use Amazon Cognito authentication for OpenSearch Dashboards\.  
*Required*: No  
*Type*: [CognitoOptions](aws-properties-opensearchservice-domain-cognitooptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainEndpointOptions`  <a name="cfn-opensearchservice-domain-domainendpointoptions"></a>
Specifies additional options for the domain endpoint, such as whether to require HTTPS for all traffic or whether to use a custom endpoint rather than the default endpoint\.  
*Required*: No  
*Type*: [DomainEndpointOptions](aws-properties-opensearchservice-domain-domainendpointoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-opensearchservice-domain-domainname"></a>
A name for the OpenSearch Service domain\. For valid values, see the [DomainName](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/configuration-api.html#configuration-api-datatypes-domainname) data type in the *Amazon OpenSearch Service Developer Guide*\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the domain name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EBSOptions`  <a name="cfn-opensearchservice-domain-ebsoptions"></a>
The configurations of Amazon Elastic Block Store \(Amazon EBS\) volumes that are attached to data nodes in the OpenSearch Service domain\. For more information, see [EBS volume size limits](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/limits.html#ebsresource) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: [EBSOptions](aws-properties-opensearchservice-domain-ebsoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionAtRestOptions`  <a name="cfn-opensearchservice-domain-encryptionatrestoptions"></a>
Whether the domain should encrypt data at rest, and if so, the AWS KMS key to use\. See [Encryption of data at rest for Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/encryption-at-rest.html)\.  
*Required*: No  
*Type*: [EncryptionAtRestOptions](aws-properties-opensearchservice-domain-encryptionatrestoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-opensearchservice-domain-engineversion"></a>
The version of OpenSearch to use\. The value must be in the format `OpenSearch_X.Y`\. If not specified, the latest version of OpenSearch is used\. For information about the versions that OpenSearch Service supports, see [Supported versions of OpenSearch and Elasticsearch](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html#choosing-version) in the *Amazon OpenSearch Service Developer Guide*\.  
If you set the [EnableVersionUpgrade](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html#cfn-attributes-updatepolicy-upgradeopensearchdomain) update policy to `true`, you can update `EngineVersion` without interruption\. When `EnableVersionUpgrade` is set to `false`, or is not specified, updating `EngineVersion` results in [replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogPublishingOptions`  <a name="cfn-opensearchservice-domain-logpublishingoptions"></a>
An object with one or more of the following keys: `SEARCH_SLOW_LOGS`, `APPLICATION_LOGS`, `INDEX_SLOW_LOGS`, `AUDIT_LOGS`, depending on the types of logs you want to publish\. Each key needs a valid `LogPublishingOption` value\. For the full syntax, see the [examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html#aws-resource-opensearchservice-domain--examples)\.  
*Required*: No  
*Type*: Map of [LogPublishingOption](aws-properties-opensearchservice-domain-logpublishingoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NodeToNodeEncryptionOptions`  <a name="cfn-opensearchservice-domain-nodetonodeencryptionoptions"></a>
Specifies whether node\-to\-node encryption is enabled\. See [Node\-to\-node encryption for Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ntn.html)\.  
*Required*: No  
*Type*: [NodeToNodeEncryptionOptions](aws-properties-opensearchservice-domain-nodetonodeencryptionoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotOptions`  <a name="cfn-opensearchservice-domain-snapshotoptions"></a>
**DEPRECATED**\. The automated snapshot configuration for the OpenSearch Service domain indices\.  
*Required*: No  
*Type*: [SnapshotOptions](aws-properties-opensearchservice-domain-snapshotoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-opensearchservice-domain-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with the OpenSearch Service domain\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VPCOptions`  <a name="cfn-opensearchservice-domain-vpcoptions"></a>
The virtual private cloud \(VPC\) configuration for the OpenSearch Service domain\. For more information, see [Launching your Amazon OpenSearch Service domains within a VPC](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html) in the *Amazon OpenSearch Service Developer Guide*\.  
*Required*: No  
*Type*: [VPCOptions](aws-properties-opensearchservice-domain-vpcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-opensearchservice-domain-return-values"></a>

### Ref<a name="aws-resource-opensearchservice-domain-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the resource name, such as `mystack-abc1d2efg3h4.` For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opensearchservice-domain-return-values-fn--getatt"></a>

Fn::GetAtt returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-opensearchservice-domain-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the domain, such as `arn:aws:es:us-west-2:123456789012:domain/mystack-1ab2cdefghij`\. This returned value is the same as the one returned by `AWS::OpenSearchService::Domain.DomainArn`\.

`DomainEndpoint`  <a name="DomainEndpoint-fn::getatt"></a>
The domain\-specific endpoint used for requests to the OpenSearch APIs, such as `search-mystack-1ab2cdefghij-ab1c2deckoyb3hofw7wpqa3cm.us-west-1.es.amazonaws.com`\.

`Id`  <a name="Id-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-opensearchservice-domain--examples"></a>



### Create an OpenSearch Service domain that contains two data nodes and three master nodes<a name="aws-resource-opensearchservice-domain--examples--Create_an_OpenSearch_Service_domain_that_contains_two_data_nodes_and_three_master_nodes"></a>

The following example creates an OpenSearch Service domain running OpenSearch 1\.0 that contains two data nodes and three dedicated master nodes\. The domain has 40 GiB of storage and enables log publishing for application logs, search slow logs, and index slow logs\. The access policy permits the root user for the AWS account to make all HTTP requests to the domain, such as indexing documents or searching indices\.

#### JSON<a name="aws-resource-opensearchservice-domain--examples--Create_an_OpenSearch_Service_domain_that_contains_two_data_nodes_and_three_master_nodes--json"></a>

```
"OpenSearchServiceDomain": {
   "Type":"AWS::OpenSearchService::Domain",
   "Properties": {
      "DomainName": "test",
      "EngineVersion": "OpenSearch_1.0",
      "ClusterConfig": {
         "DedicatedMasterEnabled": true,
         "InstanceCount": "2",
         "ZoneAwarenessEnabled": true,
         "InstanceType": "m3.medium.search",
         "DedicatedMasterType": "m3.medium.search",
         "DedicatedMasterCount": "3"
      },
      "EBSOptions":{
         "EBSEnabled": true,
         "Iops": "0",
         "VolumeSize": "20",
         "VolumeType": "gp2"
      },
      "AccessPolicies": {
         "Version":"2012-10-17",
         "Statement":[
            {
               "Effect": "Allow",
               "Principal": {
                  "AWS": "arn:aws:iam::123456789012:user/opensearch-user"
               },
               "Action":"es:*",
               "Resource": "arn:aws:es:us-east-1:123456789012:domain/test/*"
            }
         ]
      },
      "LogPublishingOptions": {
         "APPLICATION_LOGS": {
           "CloudWatchLogsLogGroupArn": "arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-application-logs",
           "Enabled": true
         },
         "SEARCH_SLOW_LOGS": {
           "CloudWatchLogsLogGroupArn": "arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-slow-logs",
           "Enabled": true
         },
         "INDEX_SLOW_LOGS": {
           "CloudWatchLogsLogGroupArn": "arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-index-slow-logs",
           "Enabled": true
         }
      },
      "AdvancedOptions": {
         "rest.action.multi.allow_explicit_index": true,
         "override_main_response_version": true
      }
   }
}
```

#### YAML<a name="aws-resource-opensearchservice-domain--examples--Create_an_OpenSearch_Service_domain_that_contains_two_data_nodes_and_three_master_nodes--yaml"></a>

```
OpenSearchServiceDomain:
  Type: AWS::OpenSearchService::Domain
  Properties:
    DomainName: 'test'
    EngineVersion: 'OpenSearch_1.0'
    ClusterConfig:
      DedicatedMasterEnabled: true
      InstanceCount: '2'
      ZoneAwarenessEnabled: true
      InstanceType: 'm3.medium.search'
      DedicatedMasterType: 'm3.medium.search'
      DedicatedMasterCount: '3'
    EBSOptions:
      EBSEnabled: true
      Iops: '0'
      VolumeSize: '20'
      VolumeType: 'gp2'
    AccessPolicies:
      Version: '2012-10-17'
      Statement:
        -
          Effect: 'Allow'
          Principal:
            AWS: 'arn:aws:iam::123456789012:user/opensearch-user'
          Action: 'es:*'
          Resource: 'arn:aws:es:us-east-1:846973539254:domain/test/*'
    LogPublishingOptions:
      APPLICATION_LOGS:
          CloudWatchLogsLogGroupArn: 'arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-application-logs'
          Enabled: true
      SEARCH_SLOW_LOGS:
          CloudWatchLogsLogGroupArn: 'arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-slow-logs'
          Enabled: true
      INDEX_SLOW_LOGS:
          CloudWatchLogsLogGroupArn: 'arn:aws:logs:us-east-1:123456789012:log-group:/aws/opensearch/domains/opensearch-index-slow-logs'
          Enabled: true
    AdvancedOptions:
      rest.action.multi.allow_explicit_index: true
      override_main_response_version: true
```

### Create a domain with VPC options<a name="aws-resource-opensearchservice-domain--examples--Create_a_domain_with_VPC_options"></a>

The following example creates a domain with VPC options\.

#### JSON<a name="aws-resource-opensearchservice-domain--examples--Create_a_domain_with_VPC_options--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "OpenSearchServiceDomain resource",
  "Parameters": {
    "DomainName": {
      "Description": "User-defined OpenSearch domain name",
      "Type": "String"
    },
    "EngineVersion": {
      "Description": "User-defined OpenSearch version",
      "Type": "String"
    },
    "InstanceType": {
      "Type": "String"
    },
    "AvailabilityZone": {
      "Type": "String"
    },
    "CidrBlock": {
      "Type": "String"
    },
    "GroupDescription": {
      "Type": "String"
    },
    "SGName": {
      "Type": "String"
    }
  },
  "Resources": {
    "OpenSearchServiceDomain": {
      "Type": "AWS::OpenSearchService::Domain",
      "Properties": {
        "DomainName": {
          "Ref": "DomainName"
        },
        "EngineVersion": {
          "Ref": "EngineVersion"
        },
        "ClusterConfig": {
          "InstanceCount": "1",
          "InstanceType": {
            "Ref": "InstanceType"
          }
        },
        "EBSOptions": {
          "EBSEnabled": true,
          "Iops": "0",
          "VolumeSize": "10",
          "VolumeType": "standard"
        },
        "AccessPolicies": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Deny",
              "Principal": {
                "AWS": "*"
              },
              "Action": "es:*",
              "Resource": "*"
            }
          ]
        },
        "AdvancedOptions": {
          "rest.action.multi.allow_explicit_index": true,
          "override_main_response_version": true
        },
        "Tags": [
          {
            "Key": "foo",
            "Value": "bar"
          }
        ],
        "VPCOptions": {
          "SubnetIds": [
            {
              "Ref": "subnet"
            }
          ],
          "SecurityGroupIds": [
            {
              "Ref": "mySecurityGroup"
            }
          ]
        }
      }
    },
    "vpc": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": "10.0.0.0/16"
      }
    },
    "subnet": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId": {
          "Ref": "vpc"
        },
        "CidrBlock": {
          "Ref": "CidrBlock"
        },
        "AvailabilityZone": {
          "Ref": "AvailabilityZone"
        }
      }
    },
    "mySecurityGroup": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "GroupDescription": {
          "Ref": "GroupDescription"
        },
        "VpcId": {
          "Ref": "vpc"
        },
        "GroupName": {
          "Ref": "SGName"
        },
        "SecurityGroupIngress": [
          {
            "FromPort": 443,
            "IpProtocol": "tcp",
            "ToPort": 443,
            "CidrIp": "0.0.0.0/0"
          }
        ]
      }
    }
  },
  "Outputs": {
    "DomainArn": {
      "Value": {
        "Fn::GetAtt": [
          "OpenSearchServiceDomain",
          "DomainArn"
        ]
      }
    },
    "DomainEndpoint": {
      "Value": {
        "Fn::GetAtt": [
          "OpenSearchServiceDomain",
          "DomainEndpoint"
        ]
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

#### YAML<a name="aws-resource-opensearchservice-domain--examples--Create_a_domain_with_VPC_options--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: OpenSearchServiceDomain resource
Parameters:
  DomainName:
    Description: User-defined OpenSearch domain name
    Type: String
  EngineVersion:
    Description: User-defined OpenSearch version
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
  OpenSearchServiceDomain:
    Type: 'AWS::OpenSearchService::Domain'
    Properties:
      DomainName:
        Ref: DomainName
      EngineVersion:
        Ref: EngineVersion
      ClusterConfig:
        InstanceCount: '1'
        InstanceType:
          Ref: InstanceType
      EBSOptions:
        EBSEnabled: true
        Iops: '0'
        VolumeSize: '10'
        VolumeType: 'standard'
      AccessPolicies:
        Version: '2012-10-17'
        Statement:
          - Effect: Deny
            Principal:
              AWS: '*'
            Action: 'es:*'
            Resource: '*'
      AdvancedOptions:
        rest.action.multi.allow_explicit_index: true
        override_main_response_version: true
      Tags:
        - Key: foo
          Value: bar
      VPCOptions:
        SubnetIds:
          - Ref: subnet
        SecurityGroupIds:
          - Ref: mySecurityGroup
  vpc:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: 10.0.0.0/16
  subnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId:
        Ref: vpc
      CidrBlock:
        Ref: CidrBlock
      AvailabilityZone:
        Ref: AvailabilityZone
  mySecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription:
        Ref: GroupDescription
      VpcId:
        Ref: vpc
      GroupName:
        Ref: SGName
      SecurityGroupIngress:
        - FromPort: 443
          IpProtocol: tcp
          ToPort: 443
          CidrIp: 0.0.0.0/0
Outputs:
  DomainArn:
    Value:
      'Fn::GetAtt':
        - OpenSearchServiceDomain
        - DomainArn
  DomainEndpoint:
    Value:
      'Fn::GetAtt':
        - OpenSearchServiceDomain
        - DomainEndpoint
  SecurityGroupId:
    Value:
      Ref: mySecurityGroup
  SubnetId:
    Value:
      Ref: subnet
```