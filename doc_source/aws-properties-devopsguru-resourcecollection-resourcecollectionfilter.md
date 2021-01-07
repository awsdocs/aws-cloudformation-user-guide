# AWS::DevOpsGuru::ResourceCollection ResourceCollectionFilter<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter"></a>

 Information about a filter used to specify which AWS resources are analyzed for anomalous behavior by DevOps Guru\. 

## Syntax<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax.json"></a>

```
{
  "[CloudFormation](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation)" : CloudFormationCollectionFilter
}
```

### YAML<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax.yaml"></a>

```
  [CloudFormation](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation): 
    CloudFormationCollectionFilter
```

## Properties<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-properties"></a>

`CloudFormation`  <a name="cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation"></a>
 Information about AWS CloudFormation stacks\. You can use stacks to specify which AWS resources in your account to analyze\. For more information, see [Stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html) in the *AWS CloudFormation User Guide*\.   
*Required*: No  
*Type*: [CloudFormationCollectionFilter](aws-properties-devopsguru-resourcecollection-cloudformationcollectionfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)