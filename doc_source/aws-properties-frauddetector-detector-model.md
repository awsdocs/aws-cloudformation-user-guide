# AWS::FraudDetector::Detector Model<a name="aws-properties-frauddetector-detector-model"></a>

The model\.

## Syntax<a name="aws-properties-frauddetector-detector-model-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-frauddetector-detector-model-syntax.json"></a>

```
{
  "[Arn](#cfn-frauddetector-detector-model-arn)" : String
}
```

### YAML<a name="aws-properties-frauddetector-detector-model-syntax.yaml"></a>

```
  [Arn](#cfn-frauddetector-detector-model-arn): String
```

## Properties<a name="aws-properties-frauddetector-detector-model-properties"></a>

`Arn`  <a name="cfn-frauddetector-detector-model-arn"></a>
The ARN of the model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn\:aws[a-z-]{0,15}\:frauddetector\:[a-z0-9-]{3,20}\:[0-9]{12}\:[^\s]{2,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)