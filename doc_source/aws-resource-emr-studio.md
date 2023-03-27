# AWS::EMR::Studio<a name="aws-resource-emr-studio"></a>

The `AWS::EMR::Studio` resource specifies an Amazon EMR Studio\. An EMR Studio is a web\-based, integrated development environment for fully managed Jupyter notebooks that run on Amazon EMR clusters\. For more information, see the [https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio.html](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-studio.html)\.

## Syntax<a name="aws-resource-emr-studio-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-studio-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::Studio",
  "Properties" : {
      "[AuthMode](#cfn-emr-studio-authmode)" : String,
      "[DefaultS3Location](#cfn-emr-studio-defaults3location)" : String,
      "[Description](#cfn-emr-studio-description)" : String,
      "[EngineSecurityGroupId](#cfn-emr-studio-enginesecuritygroupid)" : String,
      "[IdpAuthUrl](#cfn-emr-studio-idpauthurl)" : String,
      "[IdpRelayStateParameterName](#cfn-emr-studio-idprelaystateparametername)" : String,
      "[Name](#cfn-emr-studio-name)" : String,
      "[ServiceRole](#cfn-emr-studio-servicerole)" : String,
      "[SubnetIds](#cfn-emr-studio-subnetids)" : [ String, ... ],
      "[Tags](#cfn-emr-studio-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserRole](#cfn-emr-studio-userrole)" : String,
      "[VpcId](#cfn-emr-studio-vpcid)" : String,
      "[WorkspaceSecurityGroupId](#cfn-emr-studio-workspacesecuritygroupid)" : String
    }
}
```

### YAML<a name="aws-resource-emr-studio-syntax.yaml"></a>

```
Type: AWS::EMR::Studio
Properties: 
  [AuthMode](#cfn-emr-studio-authmode): String
  [DefaultS3Location](#cfn-emr-studio-defaults3location): String
  [Description](#cfn-emr-studio-description): String
  [EngineSecurityGroupId](#cfn-emr-studio-enginesecuritygroupid): String
  [IdpAuthUrl](#cfn-emr-studio-idpauthurl): String
  [IdpRelayStateParameterName](#cfn-emr-studio-idprelaystateparametername): String
  [Name](#cfn-emr-studio-name): String
  [ServiceRole](#cfn-emr-studio-servicerole): String
  [SubnetIds](#cfn-emr-studio-subnetids): 
    - String
  [Tags](#cfn-emr-studio-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserRole](#cfn-emr-studio-userrole): String
  [VpcId](#cfn-emr-studio-vpcid): String
  [WorkspaceSecurityGroupId](#cfn-emr-studio-workspacesecuritygroupid): String
```

## Properties<a name="aws-resource-emr-studio-properties"></a>

`AuthMode`  <a name="cfn-emr-studio-authmode"></a>
Specifies whether the Studio authenticates users using IAM Identity Center or IAM\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `IAM | SSO`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultS3Location`  <a name="cfn-emr-studio-defaults3location"></a>
The Amazon S3 location to back up EMR Studio Workspaces and notebook files\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-emr-studio-description"></a>
A detailed description of the Amazon EMR Studio\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineSecurityGroupId`  <a name="cfn-emr-studio-enginesecuritygroupid"></a>
The ID of the Amazon EMR Studio Engine security group\. The Engine security group allows inbound network traffic from the Workspace security group, and it must be in the same VPC specified by `VpcId`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdpAuthUrl`  <a name="cfn-emr-studio-idpauthurl"></a>
Your identity provider's authentication endpoint\. Amazon EMR Studio redirects federated users to this endpoint for authentication when logging in to a Studio with the Studio URL\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdpRelayStateParameterName`  <a name="cfn-emr-studio-idprelaystateparametername"></a>
The name of your identity provider's `RelayState` parameter\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-emr-studio-name"></a>
A descriptive name for the Amazon EMR Studio\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRole`  <a name="cfn-emr-studio-servicerole"></a>
The Amazon Resource Name \(ARN\) of the IAM role that will be assumed by the Amazon EMR Studio\. The service role provides a way for Amazon EMR Studio to interoperate with other AWS services\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-emr-studio-subnetids"></a>
A list of subnet IDs to associate with the Amazon EMR Studio\. A Studio can have a maximum of 5 subnets\. The subnets must belong to the VPC specified by `VpcId`\. Studio users can create a Workspace in any of the specified subnets\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-emr-studio-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserRole`  <a name="cfn-emr-studio-userrole"></a>
The Amazon Resource Name \(ARN\) of the IAM user role that will be assumed by users and groups logged in to a Studio\. The permissions attached to this IAM role can be scoped down for each user or group using session policies\. You only need to specify `UserRole` when you set `AuthMode` to `SSO`\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-emr-studio-vpcid"></a>
The ID of the Amazon Virtual Private Cloud \(Amazon VPC\) to associate with the Studio\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WorkspaceSecurityGroupId`  <a name="cfn-emr-studio-workspacesecuritygroupid"></a>
The ID of the Workspace security group associated with the Amazon EMR Studio\. The Workspace security group allows outbound network traffic to resources in the Engine security group and to the internet\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-emr-studio-return-values"></a>

### Ref<a name="aws-resource-emr-studio-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For example:

 `{ "Ref": "es-EXAMPLE12345678XXXXXXXXXXX" }` 

Ref returns the ID of the Amazon EMR Studio\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-emr-studio-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-emr-studio-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon EMR Studio\. For example: `arn:aws:elasticmapreduce:us-east-1:653XXXXXXXXX:studio/es-EXAMPLE12345678XXXXXXXXXXX`\.

`StudioId`  <a name="StudioId-fn::getatt"></a>
The ID of the Amazon EMR Studio\. For example: `es-EXAMPLE12345678XXXXXXXXXXX`\.

`Url`  <a name="Url-fn::getatt"></a>
The unique access URL of the Amazon EMR Studio\. For example: `https://es-EXAMPLE12345678XXXXXXXXXXX.emrstudio-prod.us-east-1.amazonaws.com`\.