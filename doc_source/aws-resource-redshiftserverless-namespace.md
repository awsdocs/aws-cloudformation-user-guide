# AWS::RedshiftServerless::Namespace<a name="aws-resource-redshiftserverless-namespace"></a>

A collection of database objects and users\.

## Syntax<a name="aws-resource-redshiftserverless-namespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshiftserverless-namespace-syntax.json"></a>

```
{
  "Type" : "AWS::RedshiftServerless::Namespace",
  "Properties" : {
      "[AdminUsername](#cfn-redshiftserverless-namespace-adminusername)" : String,
      "[AdminUserPassword](#cfn-redshiftserverless-namespace-adminuserpassword)" : String,
      "[DbName](#cfn-redshiftserverless-namespace-dbname)" : String,
      "[DefaultIamRoleArn](#cfn-redshiftserverless-namespace-defaultiamrolearn)" : String,
      "[FinalSnapshotName](#cfn-redshiftserverless-namespace-finalsnapshotname)" : String,
      "[FinalSnapshotRetentionPeriod](#cfn-redshiftserverless-namespace-finalsnapshotretentionperiod)" : Integer,
      "[IamRoles](#cfn-redshiftserverless-namespace-iamroles)" : [ String, ... ],
      "[KmsKeyId](#cfn-redshiftserverless-namespace-kmskeyid)" : String,
      "[LogExports](#cfn-redshiftserverless-namespace-logexports)" : [ String, ... ],
      "[NamespaceName](#cfn-redshiftserverless-namespace-namespacename)" : String,
      "[Tags](#cfn-redshiftserverless-namespace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-redshiftserverless-namespace-syntax.yaml"></a>

```
Type: AWS::RedshiftServerless::Namespace
Properties: 
  [AdminUsername](#cfn-redshiftserverless-namespace-adminusername): String
  [AdminUserPassword](#cfn-redshiftserverless-namespace-adminuserpassword): String
  [DbName](#cfn-redshiftserverless-namespace-dbname): String
  [DefaultIamRoleArn](#cfn-redshiftserverless-namespace-defaultiamrolearn): String
  [FinalSnapshotName](#cfn-redshiftserverless-namespace-finalsnapshotname): String
  [FinalSnapshotRetentionPeriod](#cfn-redshiftserverless-namespace-finalsnapshotretentionperiod): Integer
  [IamRoles](#cfn-redshiftserverless-namespace-iamroles): 
    - String
  [KmsKeyId](#cfn-redshiftserverless-namespace-kmskeyid): String
  [LogExports](#cfn-redshiftserverless-namespace-logexports): 
    - String
  [NamespaceName](#cfn-redshiftserverless-namespace-namespacename): String
  [Tags](#cfn-redshiftserverless-namespace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-redshiftserverless-namespace-properties"></a>

`AdminUsername`  <a name="cfn-redshiftserverless-namespace-adminusername"></a>
The username of the administrator for the primary database created in the namespace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdminUserPassword`  <a name="cfn-redshiftserverless-namespace-adminuserpassword"></a>
The password of the administrator for the primary database created in the namespace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DbName`  <a name="cfn-redshiftserverless-namespace-dbname"></a>
The name of the primary database created in the namespace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultIamRoleArn`  <a name="cfn-redshiftserverless-namespace-defaultiamrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to set as a default in the namespace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FinalSnapshotName`  <a name="cfn-redshiftserverless-namespace-finalsnapshotname"></a>
The name of the snapshot to be created before the namespace is deleted\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FinalSnapshotRetentionPeriod`  <a name="cfn-redshiftserverless-namespace-finalsnapshotretentionperiod"></a>
How long to retain the final snapshot\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoles`  <a name="cfn-redshiftserverless-namespace-iamroles"></a>
A list of IAM roles to associate with the namespace\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-redshiftserverless-namespace-kmskeyid"></a>
The ID of the AWS Key Management Service key used to encrypt your data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogExports`  <a name="cfn-redshiftserverless-namespace-logexports"></a>
The types of logs the namespace can export\. Available export types are `userlog`, `connectionlog`, and `useractivitylog`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamespaceName`  <a name="cfn-redshiftserverless-namespace-namespacename"></a>
The name of the namespace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-redshiftserverless-namespace-tags"></a>
The map of the key\-value pairs used to tag the namespace\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-redshiftserverless-namespace-return-values"></a>

### Ref<a name="aws-resource-redshiftserverless-namespace-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the NamespaceName, such as `sample-namespace.` For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-redshiftserverless-namespace-return-values-fn--getatt"></a>

GetAtt returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-redshiftserverless-namespace-return-values-fn--getatt-fn--getatt"></a>

`Namespace`  <a name="Namespace-fn::getatt"></a>
Returns the `Namespace` value\.

`Namespace.AdminUsername`  <a name="Namespace.AdminUsername-fn::getatt"></a>
Property description not available\.

`Namespace.CreationDate`  <a name="Namespace.CreationDate-fn::getatt"></a>
Property description not available\.

`Namespace.DbName`  <a name="Namespace.DbName-fn::getatt"></a>
Property description not available\.

`Namespace.DefaultIamRoleArn`  <a name="Namespace.DefaultIamRoleArn-fn::getatt"></a>
Property description not available\.

`Namespace.IamRoles`  <a name="Namespace.IamRoles-fn::getatt"></a>
Property description not available\.

`Namespace.KmsKeyId`  <a name="Namespace.KmsKeyId-fn::getatt"></a>
Property description not available\.

`Namespace.LogExports`  <a name="Namespace.LogExports-fn::getatt"></a>
Property description not available\.

`Namespace.NamespaceArn`  <a name="Namespace.NamespaceArn-fn::getatt"></a>
Property description not available\.

`Namespace.NamespaceId`  <a name="Namespace.NamespaceId-fn::getatt"></a>
Property description not available\.

`Namespace.NamespaceName`  <a name="Namespace.NamespaceName-fn::getatt"></a>
Property description not available\.

`Namespace.Status`  <a name="Namespace.Status-fn::getatt"></a>
Property description not available\.