# AWS::Proton::EnvironmentAccountConnection<a name="aws-resource-proton-environmentaccountconnection"></a>

Detailed data of an AWS Proton environment account connection resource\.

## Syntax<a name="aws-resource-proton-environmentaccountconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-proton-environmentaccountconnection-syntax.json"></a>

```
{
  "Type" : "AWS::Proton::EnvironmentAccountConnection",
  "Properties" : {
      "[CodebuildRoleArn](#cfn-proton-environmentaccountconnection-codebuildrolearn)" : String,
      "[ComponentRoleArn](#cfn-proton-environmentaccountconnection-componentrolearn)" : String,
      "[EnvironmentAccountId](#cfn-proton-environmentaccountconnection-environmentaccountid)" : String,
      "[EnvironmentName](#cfn-proton-environmentaccountconnection-environmentname)" : String,
      "[ManagementAccountId](#cfn-proton-environmentaccountconnection-managementaccountid)" : String,
      "[RoleArn](#cfn-proton-environmentaccountconnection-rolearn)" : String,
      "[Tags](#cfn-proton-environmentaccountconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-proton-environmentaccountconnection-syntax.yaml"></a>

```
Type: AWS::Proton::EnvironmentAccountConnection
Properties: 
  [CodebuildRoleArn](#cfn-proton-environmentaccountconnection-codebuildrolearn): String
  [ComponentRoleArn](#cfn-proton-environmentaccountconnection-componentrolearn): String
  [EnvironmentAccountId](#cfn-proton-environmentaccountconnection-environmentaccountid): String
  [EnvironmentName](#cfn-proton-environmentaccountconnection-environmentname): String
  [ManagementAccountId](#cfn-proton-environmentaccountconnection-managementaccountid): String
  [RoleArn](#cfn-proton-environmentaccountconnection-rolearn): String
  [Tags](#cfn-proton-environmentaccountconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-proton-environmentaccountconnection-properties"></a>

`CodebuildRoleArn`  <a name="cfn-proton-environmentaccountconnection-codebuildrolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM service role in the environment account\. AWS Proton uses this role to provision infrastructure resources using CodeBuild\-based provisioning in the associated environment account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov):iam::\d{12}:role/([\w+=,.@-]{1,512}[/:])*([\w+=,.@-]{1,64})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentRoleArn`  <a name="cfn-proton-environmentaccountconnection-componentrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM service role that AWS Proton uses when provisioning directly defined components in the associated environment account\. It determines the scope of infrastructure that a component can provision in the account\.  
The environment account connection must have a `componentRoleArn` to allow directly defined components to be associated with any environments running in the account\.  
For more information about components, see [AWS Proton components](https://docs.aws.amazon.com/proton/latest/userguide/ag-components.html) in the *AWS Proton User Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov):iam::\d{12}:role/([\w+=,.@-]{1,512}[/:])*([\w+=,.@-]{1,64})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentAccountId`  <a name="cfn-proton-environmentaccountconnection-environmentaccountid"></a>
The environment account that's connected to the environment account connection\.  
*Required*: No  
*Type*: String  
*Pattern*: `^\d{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentName`  <a name="cfn-proton-environmentaccountconnection-environmentname"></a>
The name of the environment that's associated with the environment account connection\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[0-9A-Za-z]+[0-9A-Za-z_\-]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagementAccountId`  <a name="cfn-proton-environmentaccountconnection-managementaccountid"></a>
The ID of the management account that's connected to the environment account connection\.  
*Required*: No  
*Type*: String  
*Pattern*: `^\d{12}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-proton-environmentaccountconnection-rolearn"></a>
The IAM service role that's associated with the environment account connection\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov):[a-zA-Z0-9-]+:[a-zA-Z0-9-]*:\d{12}:([\w+=,.@-]+[/:])*[\w+=,.@-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-proton-environmentaccountconnection-tags"></a>
An optional list of metadata items that you can associate with the AWS Proton environment account connection\. A tag is a key\-value pair\.  
For more information, see [AWS Proton resources and tagging](https://docs.aws.amazon.com/proton/latest/userguide/resources.html) in the *AWS Proton User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-proton-environmentaccountconnection-return-values"></a>

### Ref<a name="aws-resource-proton-environmentaccountconnection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the environment account connection\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-proton-environmentaccountconnection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-proton-environmentaccountconnection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the environment account connection ARN\.

`Id`  <a name="Id-fn::getatt"></a>
Returns the environment account connection ID\.

`Status`  <a name="Status-fn::getatt"></a>
Returns the environment account connection status\.