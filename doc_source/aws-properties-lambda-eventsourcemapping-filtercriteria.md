# AWS::Lambda::EventSourceMapping FilterCriteria<a name="aws-properties-lambda-eventsourcemapping-filtercriteria"></a>

 An object that contains the filters for an event source\. 

## Syntax<a name="aws-properties-lambda-eventsourcemapping-filtercriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-filtercriteria-syntax.json"></a>

```
{
  "[Filters](#cfn-lambda-eventsourcemapping-filtercriteria-filters)" : [ Filter, ... ]
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-filtercriteria-syntax.yaml"></a>

```
  [Filters](#cfn-lambda-eventsourcemapping-filtercriteria-filters): 
    - Filter
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-filtercriteria-properties"></a>

`Filters`  <a name="cfn-lambda-eventsourcemapping-filtercriteria-filters"></a>
 A list of filters\.   
*Required*: No  
*Type*: List of [Filter](aws-properties-lambda-eventsourcemapping-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)