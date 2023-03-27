# AWS::SageMaker::App<a name="aws-resource-sagemaker-app"></a>

Creates a running app for the specified UserProfile\. This operation is automatically invoked by Amazon SageMaker Studio upon access to the associated Domain, and when new kernel configurations are selected by the user\. A user may have multiple Apps active simultaneously\.

## Syntax<a name="aws-resource-sagemaker-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-app-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::App",
  "Properties" : {
      "[AppName](#cfn-sagemaker-app-appname)" : String,
      "[AppType](#cfn-sagemaker-app-apptype)" : String,
      "[DomainId](#cfn-sagemaker-app-domainid)" : String,
      "[ResourceSpec](#cfn-sagemaker-app-resourcespec)" : ResourceSpec,
      "[Tags](#cfn-sagemaker-app-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserProfileName](#cfn-sagemaker-app-userprofilename)" : String
    }
}
```

### YAML<a name="aws-resource-sagemaker-app-syntax.yaml"></a>

```
Type: AWS::SageMaker::App
Properties: 
  [AppName](#cfn-sagemaker-app-appname): String
  [AppType](#cfn-sagemaker-app-apptype): String
  [DomainId](#cfn-sagemaker-app-domainid): String
  [ResourceSpec](#cfn-sagemaker-app-resourcespec): 
    ResourceSpec
  [Tags](#cfn-sagemaker-app-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserProfileName](#cfn-sagemaker-app-userprofilename): String
```

## Properties<a name="aws-resource-sagemaker-app-properties"></a>

`AppName`  <a name="cfn-sagemaker-app-appname"></a>
The name of the app\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AppType`  <a name="cfn-sagemaker-app-apptype"></a>
The type of app\.  
*Allowed Values*: `JupyterServer | KernelGateway | RSessionGateway | RStudioServerPro | TensorBoard | Canvas`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainId`  <a name="cfn-sagemaker-app-domainid"></a>
The domain ID\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceSpec`  <a name="cfn-sagemaker-app-resourcespec"></a>
Specifies the ARNs of a SageMaker image and SageMaker image version, and the instance type that the version runs on\.  
*Required*: No  
*Type*: [ResourceSpec](aws-properties-sagemaker-app-resourcespec.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-app-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserProfileName`  <a name="cfn-sagemaker-app-userprofilename"></a>
The user profile name\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sagemaker-app-return-values"></a>

### Ref<a name="aws-resource-sagemaker-app-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the app type, app name, Domain ID, and user profile name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-sagemaker-app-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-sagemaker-app-return-values-fn--getatt-fn--getatt"></a>

`AppArn`  <a name="AppArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the app, such as `arn:aws:sagemaker:us-west-2:account-id:app/my-app-name`\.