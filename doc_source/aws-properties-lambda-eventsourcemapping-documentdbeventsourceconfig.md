# AWS::Lambda::EventSourceMapping DocumentDBEventSourceConfig<a name="aws-properties-lambda-eventsourcemapping-documentdbeventsourceconfig"></a>

 Specific configuration settings for a DocumentDB event source\. 

## Syntax<a name="aws-properties-lambda-eventsourcemapping-documentdbeventsourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-documentdbeventsourceconfig-syntax.json"></a>

```
{
  "[CollectionName](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-collectionname)" : String,
  "[DatabaseName](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-databasename)" : String,
  "[FullDocument](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-fulldocument)" : String
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-documentdbeventsourceconfig-syntax.yaml"></a>

```
  [CollectionName](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-collectionname): String
  [DatabaseName](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-databasename): String
  [FullDocument](#cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-fulldocument): String
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-documentdbeventsourceconfig-properties"></a>

`CollectionName`  <a name="cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-collectionname"></a>
 The name of the collection to consume within the database\. If you do not specify a collection, Lambda consumes all collections\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `57`  
*Pattern*: `(^(?!(system\x2e)))(^[_a-zA-Z0-9])([^$]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-databasename"></a>
 The name of the database to consume within the DocumentDB cluster\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `[^ /\.$\x22]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullDocument`  <a name="cfn-lambda-eventsourcemapping-documentdbeventsourceconfig-fulldocument"></a>
 Determines what DocumentDB sends to your event stream during document update operations\. If set to UpdateLookup, DocumentDB sends a delta describing the changes, along with a copy of the entire document\. Otherwise, DocumentDB sends only a partial document that contains the changes\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Default | UpdateLookup`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)