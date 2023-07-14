# AWS::ECR::ReplicationConfiguration<a name="aws-resource-ecr-replicationconfiguration"></a>

The `AWS::ECR::ReplicationConfiguration` resource creates or updates the replication configuration for a private registry\. The first time a replication configuration is applied to a private registry, a service\-linked IAM role is created in your account for the replication process\. For more information, see [Using Service\-Linked Roles for Amazon ECR](https://docs.aws.amazon.com/AmazonECR/latest/userguide/using-service-linked-roles.html) in the *Amazon Elastic Container Registry User Guide*\.

**Note**  
When configuring cross\-account replication, the destination account must grant the source account permission to replicate\. This permission is controlled using a private registry permissions policy\. For more information, see `AWS::ECR::RegistryPolicy`\.

## Syntax<a name="aws-resource-ecr-replicationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-replicationconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::ReplicationConfiguration",
  "Properties" : {
      "[ReplicationConfiguration](#cfn-ecr-replicationconfiguration-replicationconfiguration)" : ReplicationConfiguration
    }
}
```

### YAML<a name="aws-resource-ecr-replicationconfiguration-syntax.yaml"></a>

```
Type: AWS::ECR::ReplicationConfiguration
Properties: 
  [ReplicationConfiguration](#cfn-ecr-replicationconfiguration-replicationconfiguration): 
    ReplicationConfiguration
```

## Properties<a name="aws-resource-ecr-replicationconfiguration-properties"></a>

`ReplicationConfiguration`  <a name="cfn-ecr-replicationconfiguration-replicationconfiguration"></a>
The replication configuration for a registry\.  
*Required*: Yes  
*Type*: [ReplicationConfiguration](aws-properties-ecr-replicationconfiguration-replicationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecr-replicationconfiguration-return-values"></a>

### Fn::GetAtt<a name="aws-resource-ecr-replicationconfiguration-return-values-fn--getatt"></a>

#### <a name="aws-resource-ecr-replicationconfiguration-return-values-fn--getatt-fn--getatt"></a>

`RegistryId`  <a name="RegistryId-fn::getatt"></a>
The account ID of the destination registry\.

## Examples<a name="aws-resource-ecr-replicationconfiguration--examples"></a>



### Specify a replication configuration for a private registry<a name="aws-resource-ecr-replicationconfiguration--examples--Specify_a_replication_configuration_for_a_private_registry"></a>

The following example specifies a replication configuration in a source Region for a private registry to replicate the contents to the `us-east-2` and `us-west-1` Regions within the same account\.

#### JSON<a name="aws-resource-ecr-replicationconfiguration--examples--Specify_a_replication_configuration_for_a_private_registry--json"></a>

```
"TestReplicationConfiguration": {
  "Type": "AWS::ECR::ReplicationConfiguration",
  "Properties": {
     "ReplicationConfiguration": {
        "Rules": [
           {
              "Destinations": [
                 {
                    "Region": "us-east-2",
                    "RegistryId": "123456789012"
                 },
                 {
                     "Region": "us-west-1",
                     "RegistryId": "123456789012"
                 }
               ]
             }
          ]
       }
    }
}
```

#### YAML<a name="aws-resource-ecr-replicationconfiguration--examples--Specify_a_replication_configuration_for_a_private_registry--yaml"></a>

```
Resources:
  MyReplicationConfig:
    Type: AWS::ECR::ReplicationConfiguration
    Properties:
      ReplicationConfiguration: 
          Rules:
            - Destinations:
                - Region: "us-east-2"
                  RegistryId: "123456789012"
                - Region: "us-west-1"
                  RegistryId: "123456789012"
```