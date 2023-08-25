# AWS::EMR::WALWorkspace<a name="aws-resource-emr-walworkspace"></a>

A WAL workspace is a logical container of write\-ahead logs \(WALs\)\. All WALs in Amazon EMR WAL are encapsulated by a WAL workspace\. 

## Syntax<a name="aws-resource-emr-walworkspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-walworkspace-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::WALWorkspace",
  "Properties" : {
      "[Tags](#cfn-emr-walworkspace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WALWorkspaceName](#cfn-emr-walworkspace-walworkspacename)" : String
    }
}
```

### YAML<a name="aws-resource-emr-walworkspace-syntax.yaml"></a>

```
Type: AWS::EMR::WALWorkspace
Properties: 
  [Tags](#cfn-emr-walworkspace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WALWorkspaceName](#cfn-emr-walworkspace-walworkspacename): String
```

## Properties<a name="aws-resource-emr-walworkspace-properties"></a>

`Tags`  <a name="cfn-emr-walworkspace-tags"></a>
You can add tags when you create a new workspace\. You can add, remove, or list tags from an active workspace, but you can't update tags\. Instead, remove the tag and add a new one\. For more information, see see [Tag your Amazon EMR WAL workspaces](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-hbase-wal.html#emr-hbase-wal-tagging)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WALWorkspaceName`  <a name="cfn-emr-walworkspace-walworkspacename"></a>
The name of the WAL workspace\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-emr-walworkspace-return-values"></a>

### Ref<a name="aws-resource-emr-walworkspace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the workspace\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.