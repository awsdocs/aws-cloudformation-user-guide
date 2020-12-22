# AWS::SageMaker::DeviceFleet<a name="aws-resource-sagemaker-devicefleet"></a>

The `AWS::SageMaker::DeviceFleet` resource is an Amazon SageMaker resource type that allows you  to create a DeviceFleet that manages your SageMaker  Edge Manager Devices\. You must register your devices against the `DeviceFleet` separately\.

## Syntax<a name="aws-resource-sagemaker-devicefleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-devicefleet-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::DeviceFleet",
  "Properties" : {
      "[Description](#cfn-sagemaker-devicefleet-description)" : String,
      "[OutputConfig](#cfn-sagemaker-devicefleet-outputconfig)" : EdgeOutputConfig,
      "[RoleArn](#cfn-sagemaker-devicefleet-rolearn)" : String,
      "[Tags](#cfn-sagemaker-devicefleet-tags)" : [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
    }
}
```

### YAML<a name="aws-resource-sagemaker-devicefleet-syntax.yaml"></a>

```
Type: AWS::SageMaker::DeviceFleet
Properties: 
  [Description](#cfn-sagemaker-devicefleet-description): String
  [OutputConfig](#cfn-sagemaker-devicefleet-outputconfig): 
    EdgeOutputConfig
  [RoleArn](#cfn-sagemaker-devicefleet-rolearn): String
  [Tags](#cfn-sagemaker-devicefleet-tags): 
    [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-devicefleet-properties"></a>

`Description`  <a name="cfn-sagemaker-devicefleet-description"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputConfig`  <a name="cfn-sagemaker-devicefleet-outputconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [EdgeOutputConfig](aws-properties-sagemaker-devicefleet-edgeoutputconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-sagemaker-devicefleet-rolearn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-devicefleet-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-devicefleet-return-values"></a>

### Ref<a name="aws-resource-sagemaker-devicefleet-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-devicefleet-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-devicefleet-return-values-fn--getatt-fn--getatt"></a>

`DeviceFleetName`  <a name="DeviceFleetName-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.