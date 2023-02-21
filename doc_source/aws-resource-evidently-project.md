# AWS::Evidently::Project<a name="aws-resource-evidently-project"></a>

Creates a project, which is the logical object in Evidently that can contain features, launches, and experiments\. Use projects to group similar features together\.

## Syntax<a name="aws-resource-evidently-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-evidently-project-syntax.json"></a>

```
{
  "Type" : "AWS::Evidently::Project",
  "Properties" : {
      "[AppConfigResource](#cfn-evidently-project-appconfigresource)" : AppConfigResourceObject,
      "[DataDelivery](#cfn-evidently-project-datadelivery)" : DataDeliveryObject,
      "[Description](#cfn-evidently-project-description)" : String,
      "[Name](#cfn-evidently-project-name)" : String,
      "[Tags](#cfn-evidently-project-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-evidently-project-syntax.yaml"></a>

```
Type: AWS::Evidently::Project
Properties: 
  [AppConfigResource](#cfn-evidently-project-appconfigresource): 
    AppConfigResourceObject
  [DataDelivery](#cfn-evidently-project-datadelivery): 
    DataDeliveryObject
  [Description](#cfn-evidently-project-description): String
  [Name](#cfn-evidently-project-name): String
  [Tags](#cfn-evidently-project-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-evidently-project-properties"></a>

`AppConfigResource`  <a name="cfn-evidently-project-appconfigresource"></a>
Use this parameter if the project will use *client\-side evaluation powered by AWS AppConfig*\. Client\-side evaluation allows your application to assign variations to user sessions locally instead of by calling the [EvaluateFeature](https://docs.aws.amazon.com/cloudwatchevidently/latest/APIReference/API_EvaluateFeature.html) operation\. This mitigates the latency and availability risks that come with an API call\. For more information, see [ Use client\-side evaluation \- powered by AWS AppConfig\.](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-client-side-evaluation.html)  
This parameter is a structure that contains information about the AWS AppConfig application that will be used as for client\-side evaluation\.  
To create a project that uses client\-side evaluation, you must have the `evidently:ExportProjectAsConfiguration` permission\.  
*Required*: No  
*Type*: [AppConfigResourceObject](aws-properties-evidently-project-appconfigresourceobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataDelivery`  <a name="cfn-evidently-project-datadelivery"></a>
A structure that contains information about where Evidently is to store evaluation events for longer term storage, if you choose to do so\. If you choose not to store these events, Evidently deletes them after using them to produce metrics and other experiment results that you can view\.  
You can't specify both `CloudWatchLogs` and `S3Destination` in the same operation\.  
*Required*: No  
*Type*: [DataDeliveryObject](aws-properties-evidently-project-datadeliveryobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-evidently-project-description"></a>
An optional description of the project\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-evidently-project-name"></a>
The name for the project\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-evidently-project-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the project\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with a project\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-evidently-project-return-values"></a>

### Ref<a name="aws-resource-evidently-project-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the project\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-evidently-project-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-evidently-project-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the project\. For example, `arn:aws:evidently:us-west-2:0123455678912:project/myProject`