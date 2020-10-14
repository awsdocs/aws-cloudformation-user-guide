# AWS::ECS::TaskDefinition AuthorizationConfig<a name="aws-properties-ecs-taskdefinition-authorizationconfig"></a>

The authorization configuration details for the Amazon EFS file system\.

## Syntax<a name="aws-properties-ecs-taskdefinition-authorizationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-authorizationconfig-syntax.json"></a>

```
{
  "[AccessPointId](#cfn-ecs-taskdefinition-authorizationconfig-accesspointid)" : String,
  "[IAM](#cfn-ecs-taskdefinition-authorizationconfig-iam)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-authorizationconfig-syntax.yaml"></a>

```
  [AccessPointId](#cfn-ecs-taskdefinition-authorizationconfig-accesspointid): String
  [IAM](#cfn-ecs-taskdefinition-authorizationconfig-iam): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-authorizationconfig-properties"></a>

`AccessPointId`  <a name="cfn-ecs-taskdefinition-authorizationconfig-accesspointid"></a>
The Amazon EFS access point ID to use\. If an access point is specified, the root directory value specified in the `EFSVolumeConfiguration` must either be omitted or set to `/` which will enforce the path set on the EFS access point\. If an access point is used, transit encryption must be enabled in the `EFSVolumeConfiguration`\. For more information, see [Working with Amazon EFS Access Points](https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IAM`  <a name="cfn-ecs-taskdefinition-authorizationconfig-iam"></a>
Whether or not to use the Amazon ECS task IAM role defined in a task definition when mounting the Amazon EFS file system\. If enabled, transit encryption must be enabled in the `EFSVolumeConfiguration`\. If this parameter is omitted, the default value of `DISABLED` is used\. For more information, see [Using Amazon EFS Access Points](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/efs-volumes.html#efs-volume-accesspoints) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)