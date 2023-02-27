# AWS::GreengrassV2::Deployment IoTJobAbortConfig<a name="aws-properties-greengrassv2-deployment-iotjobabortconfig"></a>

Contains a list of criteria that define when and how to cancel a configuration deployment\.

## Syntax<a name="aws-properties-greengrassv2-deployment-iotjobabortconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-iotjobabortconfig-syntax.json"></a>

```
{
  "[CriteriaList](#cfn-greengrassv2-deployment-iotjobabortconfig-criterialist)" : [ IoTJobAbortCriteria, ... ]
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-iotjobabortconfig-syntax.yaml"></a>

```
  [CriteriaList](#cfn-greengrassv2-deployment-iotjobabortconfig-criterialist): 
    - IoTJobAbortCriteria
```

## Properties<a name="aws-properties-greengrassv2-deployment-iotjobabortconfig-properties"></a>

`CriteriaList`  <a name="cfn-greengrassv2-deployment-iotjobabortconfig-criterialist"></a>
The list of criteria that define when and how to cancel the configuration deployment\.  
*Required*: Yes  
*Type*: List of [IoTJobAbortCriteria](aws-properties-greengrassv2-deployment-iotjobabortcriteria.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)