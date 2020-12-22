# AWS::SageMaker::Device<a name="aws-resource-sagemaker-device"></a>

The `AWS::SageMaker::Device` resource is an Amazon SageMaker resource type that allows you  to register your Devices against an existing SageMaker Edge Manager DeviceFleet\. Each device must be listed   individually in the CFN specification\.

## Syntax<a name="aws-resource-sagemaker-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sagemaker-device-syntax.json"></a>

```
{
  "Type" : "AWS::SageMaker::Device",
  "Properties" : {
      "[Device](#cfn-sagemaker-device-device)" : Device,
      "[Tags](#cfn-sagemaker-device-tags)" : [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
    }
}
```

### YAML<a name="aws-resource-sagemaker-device-syntax.yaml"></a>

```
Type: AWS::SageMaker::Device
Properties: 
  [Device](#cfn-sagemaker-device-device): 
    Device
  [Tags](#cfn-sagemaker-device-tags): 
    [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-sagemaker-device-properties"></a>

`Device`  <a name="cfn-sagemaker-device-device"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Device](aws-properties-sagemaker-device-device.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-sagemaker-device-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) of Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sagemaker-device-return-values"></a>

### Ref<a name="aws-resource-sagemaker-device-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-sagemaker-device-return-values-fn--getatt"></a>

#### <a name="aws-resource-sagemaker-device-return-values-fn--getatt-fn--getatt"></a>

`DeviceFleetName`  <a name="DeviceFleetName-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.