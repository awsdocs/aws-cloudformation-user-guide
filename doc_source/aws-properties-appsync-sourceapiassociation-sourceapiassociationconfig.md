# AWS::AppSync::SourceApiAssociation SourceApiAssociationConfig<a name="aws-properties-appsync-sourceapiassociation-sourceapiassociationconfig"></a>

Describes properties used to specify configurations related to a source API\. This is a property of the `AWS:AppSync:SourceApiAssociation` type\.

## Syntax<a name="aws-properties-appsync-sourceapiassociation-sourceapiassociationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-sourceapiassociation-sourceapiassociationconfig-syntax.json"></a>

```
{
  "[MergeType](#cfn-appsync-sourceapiassociation-sourceapiassociationconfig-mergetype)" : String
}
```

### YAML<a name="aws-properties-appsync-sourceapiassociation-sourceapiassociationconfig-syntax.yaml"></a>

```
  [MergeType](#cfn-appsync-sourceapiassociation-sourceapiassociationconfig-mergetype): String
```

## Properties<a name="aws-properties-appsync-sourceapiassociation-sourceapiassociationconfig-properties"></a>

`MergeType`  <a name="cfn-appsync-sourceapiassociation-sourceapiassociationconfig-mergetype"></a>
The property that indicates which merging option is enabled in the source API association\.  
Valid merge types are `MANUAL_MERGE` \(default\) and `AUTO_MERGE`\. Manual merges are the default behavior and require the user to trigger any changes from the source APIs to the merged API manually\. Auto merges subscribe the merged API to the changes performed on the source APIs so that any change in the source APIs are also made to the merged API\. Auto merges use `MergedApiExecutionRoleArn` to perform merge operations\.  
The following values are valid:  
`MANUAL_MERGE | AUTO_MERGE`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)