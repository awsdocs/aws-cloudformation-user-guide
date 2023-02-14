# AWS::RefactorSpaces::Service<a name="aws-resource-refactorspaces-service"></a>

Creates an AWS Migration Hub Refactor Spaces service\. The account owner of the service is always the environment owner, regardless of which account in the environment creates the service\. Services have either a URL endpoint in a virtual private cloud \(VPC\), or a Lambda function endpoint\.

**Important**  
If an AWS resource is launched in a service VPC, and you want it to be accessible to all of an environment’s services with VPCs and routes, apply the `RefactorSpacesSecurityGroup` to the resource\. Alternatively, to add more cross\-account constraints, apply your own security group\.

## Syntax<a name="aws-resource-refactorspaces-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-refactorspaces-service-syntax.json"></a>

```
{
  "Type" : "AWS::RefactorSpaces::Service",
  "Properties" : {
      "[ApplicationIdentifier](#cfn-refactorspaces-service-applicationidentifier)" : String,
      "[Description](#cfn-refactorspaces-service-description)" : String,
      "[EndpointType](#cfn-refactorspaces-service-endpointtype)" : String,
      "[EnvironmentIdentifier](#cfn-refactorspaces-service-environmentidentifier)" : String,
      "[LambdaEndpoint](#cfn-refactorspaces-service-lambdaendpoint)" : LambdaEndpointInput,
      "[Name](#cfn-refactorspaces-service-name)" : String,
      "[Tags](#cfn-refactorspaces-service-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UrlEndpoint](#cfn-refactorspaces-service-urlendpoint)" : UrlEndpointInput,
      "[VpcId](#cfn-refactorspaces-service-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-refactorspaces-service-syntax.yaml"></a>

```
Type: AWS::RefactorSpaces::Service
Properties: 
  [ApplicationIdentifier](#cfn-refactorspaces-service-applicationidentifier): String
  [Description](#cfn-refactorspaces-service-description): String
  [EndpointType](#cfn-refactorspaces-service-endpointtype): String
  [EnvironmentIdentifier](#cfn-refactorspaces-service-environmentidentifier): String
  [LambdaEndpoint](#cfn-refactorspaces-service-lambdaendpoint): 
    LambdaEndpointInput
  [Name](#cfn-refactorspaces-service-name): String
  [Tags](#cfn-refactorspaces-service-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UrlEndpoint](#cfn-refactorspaces-service-urlendpoint): 
    UrlEndpointInput
  [VpcId](#cfn-refactorspaces-service-vpcid): String
```

## Properties<a name="aws-resource-refactorspaces-service-properties"></a>

`ApplicationIdentifier`  <a name="cfn-refactorspaces-service-applicationidentifier"></a>
The unique identifier of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-refactorspaces-service-description"></a>
A description of the service\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointType`  <a name="cfn-refactorspaces-service-endpointtype"></a>
The endpoint type of the service\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnvironmentIdentifier`  <a name="cfn-refactorspaces-service-environmentidentifier"></a>
The unique identifier of the environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LambdaEndpoint`  <a name="cfn-refactorspaces-service-lambdaendpoint"></a>
A summary of the configuration for the AWS Lambda endpoint type\.   
*Required*: No  
*Type*: [LambdaEndpointInput](aws-properties-refactorspaces-service-lambdaendpointinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-refactorspaces-service-name"></a>
The name of the service\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-refactorspaces-service-tags"></a>
The tags assigned to the service\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UrlEndpoint`  <a name="cfn-refactorspaces-service-urlendpoint"></a>
The summary of the configuration for the URL endpoint type\.   
*Required*: No  
*Type*: [UrlEndpointInput](aws-properties-refactorspaces-service-urlendpointinput.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcId`  <a name="cfn-refactorspaces-service-vpcid"></a>
The ID of the virtual private cloud \(VPC\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-refactorspaces-service-return-values"></a>

### Ref<a name="aws-resource-refactorspaces-service-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a composite ID following this format: `<EnvironmentId>|<ApplicationId>|<ServiceId>`\. For example, `env-1234654123|app-1234654123|svc-1234654123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-refactorspaces-service-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-refactorspaces-service-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service\.

`ServiceIdentifier`  <a name="ServiceIdentifier-fn::getatt"></a>
The unique identifier of the service\.