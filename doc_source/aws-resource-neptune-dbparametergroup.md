# AWS::Neptune::DBParameterGroup<a name="aws-resource-neptune-dbparametergroup"></a>

 `AWS::Neptune::DBParameterGroup` creates a new DB parameter group\. This type can be declared in a template and referenced in the `DBParameterGroupName` parameter of `AWS::Neptune::DBInstance`\.

**Note**  
Applying a parameter group to a DB instance might require the instance to reboot, resulting in a database outage for the duration of the reboot\.

A DB parameter group is initially created with the default parameters for the database engine used by the DB instance\. To provide custom values for any of the parameters, you must modify the group after creating it using *ModifyDBParameterGroup*\. Once you've created a DB parameter group, you need to associate it with your DB instance using *ModifyDBInstance*\. When you associate a new DB parameter group with a running DB instance, you need to reboot the DB instance without failover for the new DB parameter group and associated settings to take effect\.

**Important**  
After you create a DB parameter group, you should wait at least 5 minutes before creating your first DB instance that uses that DB parameter group as the default parameter group\. This allows Amazon Neptune to fully complete the create action before the parameter group is used as the default for a new DB instance\. This is especially important for parameters that are critical when creating the default database for a DB instance, such as the character set for the default database defined by the `character_set_database` parameter\. You can use the *Parameter Groups* option of the Amazon Neptune console or the *DescribeDBParameters* command to verify that your DB parameter group has been created or modified\.

## Syntax<a name="aws-resource-neptune-dbparametergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbparametergroup-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBParameterGroup",
  "Properties" : {
      "[Description](#cfn-neptune-dbparametergroup-description)" : String,
      "[Family](#cfn-neptune-dbparametergroup-family)" : String,
      "[Name](#cfn-neptune-dbparametergroup-name)" : String,
      "[Parameters](#cfn-neptune-dbparametergroup-parameters)" : Json,
      "[Tags](#cfn-neptune-dbparametergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-neptune-dbparametergroup-syntax.yaml"></a>

```
Type: AWS::Neptune::DBParameterGroup
Properties: 
  [Description](#cfn-neptune-dbparametergroup-description): String
  [Family](#cfn-neptune-dbparametergroup-family): String
  [Name](#cfn-neptune-dbparametergroup-name): String
  [Parameters](#cfn-neptune-dbparametergroup-parameters): Json
  [Tags](#cfn-neptune-dbparametergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-neptune-dbparametergroup-properties"></a>

`Description`  <a name="cfn-neptune-dbparametergroup-description"></a>
Provides the customer\-specified description for this DB parameter group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Family`  <a name="cfn-neptune-dbparametergroup-family"></a>
Must be `neptune1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-neptune-dbparametergroup-name"></a>
Provides the name of the DB parameter group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-neptune-dbparametergroup-parameters"></a>
The parameters to set for this DB parameter group\.  
The parameters are expressed as a JSON object consisting of key\-value pairs\.  
Changes to dynamic parameters are applied immediately\. During an update, if you have static parameters \(whether they were changed or not\), it triggers AWS CloudFormation to reboot the associated DB instance without failover\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-neptune-dbparametergroup-tags"></a>
The tags that you want to attach to this parameter group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-neptune-dbparametergroup-return-values"></a>

### Ref<a name="aws-resource-neptune-dbparametergroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.