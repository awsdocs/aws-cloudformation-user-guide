# AWS::Pipes::Pipe PlacementStrategy<a name="aws-properties-pipes-pipe-placementstrategy"></a>

The task placement strategy for a task or service\. To learn more, see [Task Placement Strategies](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-strategies.html) in the Amazon Elastic Container Service Service Developer Guide\.

## Syntax<a name="aws-properties-pipes-pipe-placementstrategy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-placementstrategy-syntax.json"></a>

```
{
  "[Field](#cfn-pipes-pipe-placementstrategy-field)" : String,
  "[Type](#cfn-pipes-pipe-placementstrategy-type)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-placementstrategy-syntax.yaml"></a>

```
  [Field](#cfn-pipes-pipe-placementstrategy-field): String
  [Type](#cfn-pipes-pipe-placementstrategy-type): String
```

## Properties<a name="aws-properties-pipes-pipe-placementstrategy-properties"></a>

`Field`  <a name="cfn-pipes-pipe-placementstrategy-field"></a>
The field to apply the placement strategy against\. For the spread placement strategy, valid values are instanceId \(or host, which has the same effect\), or any platform or custom attribute that is applied to a container instance, such as attribute:ecs\.availability\-zone\. For the binpack placement strategy, valid values are cpu and memory\. For the random placement strategy, this field is not used\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-pipes-pipe-placementstrategy-type"></a>
The type of placement strategy\. The random placement strategy randomly places tasks on available candidates\. The spread placement strategy spreads placement across available candidates evenly based on the field parameter\. The binpack strategy places tasks on available candidates that have the least available amount of the resource that is specified with the field parameter\. For example, if you binpack on memory, a task is placed on the instance with the least amount of remaining memory \(but still enough to run the task\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)