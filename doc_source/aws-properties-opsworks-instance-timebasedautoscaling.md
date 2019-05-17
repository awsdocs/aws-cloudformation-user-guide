# AWS::OpsWorks::Instance TimeBasedAutoScaling<a name="aws-properties-opsworks-instance-timebasedautoscaling"></a>

Describes an instance's time\-based auto scaling configuration\.

## Syntax<a name="aws-properties-opsworks-instance-timebasedautoscaling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-instance-timebasedautoscaling-syntax.json"></a>

```
{
  "[Friday](#cfn-opsworks-instance-timebasedautoscaling-friday)" : {Key : Value, ...},
  "[Monday](#cfn-opsworks-instance-timebasedautoscaling-monday)" : {Key : Value, ...},
  "[Saturday](#cfn-opsworks-instance-timebasedautoscaling-saturday)" : {Key : Value, ...},
  "[Sunday](#cfn-opsworks-instance-timebasedautoscaling-sunday)" : {Key : Value, ...},
  "[Thursday](#cfn-opsworks-instance-timebasedautoscaling-thursday)" : {Key : Value, ...},
  "[Tuesday](#cfn-opsworks-instance-timebasedautoscaling-tuesday)" : {Key : Value, ...},
  "[Wednesday](#cfn-opsworks-instance-timebasedautoscaling-wednesday)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-opsworks-instance-timebasedautoscaling-syntax.yaml"></a>

```
  [Friday](#cfn-opsworks-instance-timebasedautoscaling-friday): 
    Key : Value
  [Monday](#cfn-opsworks-instance-timebasedautoscaling-monday): 
    Key : Value
  [Saturday](#cfn-opsworks-instance-timebasedautoscaling-saturday): 
    Key : Value
  [Sunday](#cfn-opsworks-instance-timebasedautoscaling-sunday): 
    Key : Value
  [Thursday](#cfn-opsworks-instance-timebasedautoscaling-thursday): 
    Key : Value
  [Tuesday](#cfn-opsworks-instance-timebasedautoscaling-tuesday): 
    Key : Value
  [Wednesday](#cfn-opsworks-instance-timebasedautoscaling-wednesday): 
    Key : Value
```

## Properties<a name="aws-properties-opsworks-instance-timebasedautoscaling-properties"></a>

`Friday`  <a name="cfn-opsworks-instance-timebasedautoscaling-friday"></a>
The schedule for Friday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Monday`  <a name="cfn-opsworks-instance-timebasedautoscaling-monday"></a>
The schedule for Monday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Saturday`  <a name="cfn-opsworks-instance-timebasedautoscaling-saturday"></a>
The schedule for Saturday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sunday`  <a name="cfn-opsworks-instance-timebasedautoscaling-sunday"></a>
The schedule for Sunday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Thursday`  <a name="cfn-opsworks-instance-timebasedautoscaling-thursday"></a>
The schedule for Thursday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tuesday`  <a name="cfn-opsworks-instance-timebasedautoscaling-tuesday"></a>
The schedule for Tuesday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Wednesday`  <a name="cfn-opsworks-instance-timebasedautoscaling-wednesday"></a>
The schedule for Wednesday\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)