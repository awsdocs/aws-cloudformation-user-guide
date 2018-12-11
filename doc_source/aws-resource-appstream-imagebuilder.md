# AWS::AppStream::ImageBuilder<a name="aws-resource-appstream-imagebuilder"></a>

The `AWS::AppStream::ImageBuilder` resource creates an image builder for Amazon AppStream 2\.0\. An image builder is a virtual machine that is used to create an image\. For more information, see [CreateImageBuilder](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateImageBuilder.html) in the *Amazon AppStream 2\.0 API Reference*\. 

## Syntax<a name="aws-resource-appstream-imagebuilder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-imagebuilder-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::ImageBuilder",
  "Properties" : {
    "[AppstreamAgentVersion](#cfn-appstream-imagebuilder-appstreamagentversion)" : String,    
    "[Description](#cfn-appstream-imagebuilder-description)" : String,
    "[DisplayName](#cfn-appstream-imagebuilder-displayname)" : String,
    "[DomainJoinInfo](#cfn-appstream-imagebuilder-domainjoininfo)" : [*DomainJoinInfo*](aws-properties-appstream-imagebuilder-domainjoininfo.md),
    "[EnableDefaultInternetAccess](#cfn-appstream-imagebuilder-enabledefaultinternetaccess)" : Boolean,
    "[ImageArn](#cfn-appstream-imagebuilder-imagearn)" : String,
    "[ImageName](#cfn-appstream-imagebuilder-imagename)" : String,
    "[InstanceType](#cfn-appstream-imagebuilder-instancetype)" : String,
    "[Name](#cfn-appstream-imagebuilder-name)" : String,
    "[VpcConfig](#cfn-appstream-imagebuilder-vpcconfig)" : [*VpcConfig*](aws-properties-appstream-imagebuilder-vpcconfig.md)
  }
}
```

### YAML<a name="aws-resource-appstream-imagebuilder-syntax.yaml"></a>

```
Type: "AWS::AppStream::ImageBuilder"
Properties:
  [AppstreamAgentVersion](#cfn-appstream-imagebuilder-appstreamagentversion): String
  [Description](#cfn-appstream-imagebuilder-description): String  
  [DisplayName](#cfn-appstream-imagebuilder-displayname): String
  [DomainJoinInfo](#cfn-appstream-imagebuilder-domainjoininfo): [*DomainJoinInfo*](aws-properties-appstream-imagebuilder-domainjoininfo.md)
  [EnableDefaultInternetAccess](#cfn-appstream-imagebuilder-enabledefaultinternetaccess): Boolean
  [ImageArn](#cfn-appstream-imagebuilder-imagearn): String
  [ImageName](#cfn-appstream-imagebuilder-imagename): String
  [InstanceType](#cfn-appstream-imagebuilder-instancetype): String
  [Name](#cfn-appstream-imagebuilder-name): String
  [VpcConfig](#cfn-appstream-imagebuilder-vpcconfig): [*VpcConfig*](aws-properties-appstream-imagebuilder-vpcconfig.md)
```

## Properties<a name="aws-resource-appstream-imagebuilder-properties"></a>

`AppstreamAgentVersion`  <a name="cfn-appstream-imagebuilder-appstreamagentversion"></a>
The version of the Amazon AppStream 2\.0 agent to use for this image builder\. To use the latest version of the agent, specify \[LATEST\]\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-appstream-imagebuilder-description"></a>
The description to display\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisplayName`  <a name="cfn-appstream-imagebuilder-displayname"></a>
The image builder name to display\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DomainJoinInfo`  <a name="cfn-appstream-imagebuilder-domainjoininfo"></a>
The name of the directory and organizational unit \(OU\) to use to join the image builder to a Microsoft Active Directory domain\.  
 *Required*: No  
 *Type*: [DomainJoinInfo](aws-properties-appstream-imagebuilder-domainjoininfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EnableDefaultInternetAccess`  <a name="cfn-appstream-imagebuilder-enabledefaultinternetaccess"></a>
Enables or disables default internet access for the image builder\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ImageArn`  <a name="cfn-appstream-imagebuilder-imagearn"></a>
The ARN of the public, private, or shared image to use\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ImageName`  <a name="cfn-appstream-imagebuilder-imagename"></a>
The name of the image used to create the image builder\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceType`  <a name="cfn-appstream-imagebuilder-instancetype"></a>
The instance type to use when launching the image builder\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-appstream-imagebuilder-name"></a>
A unique name for the image builder\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VpcConfig`  <a name="cfn-appstream-imagebuilder-vpcconfig"></a>
The VPC configuration for the image builder\. You can specify only one subnet\.  
 *Required*: No  
 *Type*: [VpcConfig](aws-properties-appstream-imagebuilder-vpcconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-appstream-imagebuilder-returnvalues"></a>

### Fn::GetAtt<a name="aws-resource-appstream-imagebuilder-fn-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`StreamingUrl`  
The URL to start an image builder streaming session, returned as a string\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## See Also<a name="aws-resource-appstream-imagebuilder-seealso"></a>
+ [CreateImageBuilder](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateImageBuilder.html) in the *Amazon AppStream 2\.0 API Reference*