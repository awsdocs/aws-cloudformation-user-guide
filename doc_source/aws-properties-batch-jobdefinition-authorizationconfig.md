# AWS::Batch::JobDefinition AuthorizationConfig<a name="aws-properties-batch-jobdefinition-authorizationconfig"></a>

The authorization configuration details for the Amazon EFS file system\.

## Syntax<a name="aws-properties-batch-jobdefinition-authorizationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-authorizationconfig-syntax.json"></a>

```
{
  "[AccessPointId](#cfn-batch-jobdefinition-authorizationconfig-accesspointid)" : String,
  "[Iam](#cfn-batch-jobdefinition-authorizationconfig-iam)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-authorizationconfig-syntax.yaml"></a>

```
  [AccessPointId](#cfn-batch-jobdefinition-authorizationconfig-accesspointid): String
  [Iam](#cfn-batch-jobdefinition-authorizationconfig-iam): String
```

## Properties<a name="aws-properties-batch-jobdefinition-authorizationconfig-properties"></a>

`AccessPointId`  <a name="cfn-batch-jobdefinition-authorizationconfig-accesspointid"></a>
The Amazon EFS access point ID to use\. If an access point is specified, the root directory value specified in the `EFSVolumeConfiguration` must either be omitted or set to `/` which enforces the path set on the EFS access point\. If an access point is used, transit encryption must be enabled in the `EFSVolumeConfiguration`\. For more information, see [Working with Amazon EFS access points](https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iam`  <a name="cfn-batch-jobdefinition-authorizationconfig-iam"></a>
Whether or not to use the AWS Batch job IAM role defined in a job definition when mounting the Amazon EFS file system\. If enabled, transit encryption must be enabled in the `EFSVolumeConfiguration`\. If this parameter is omitted, the default value of `DISABLED` is used\. For more information, see [Using Amazon EFS access points](https://docs.aws.amazon.com/batch/latest/userguide/efs-volumes.html#efs-volume-accesspoints) in the * AWS Batch User Guide*\. EFS IAM authorization requires that `TransitEncryption` be `ENABLED` and that a `JobRoleArn` is specified\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)