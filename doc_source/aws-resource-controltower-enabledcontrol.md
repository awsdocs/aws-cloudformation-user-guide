# AWS::ControlTower::EnabledControl<a name="aws-resource-controltower-enabledcontrol"></a>

The resource represents an enabled control\. It specifies an asynchronous operation that creates AWS resources on the specified organizational unit and the accounts it contains\. The resources created will vary according to the control that you specify\. 

## Syntax<a name="aws-resource-controltower-enabledcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-controltower-enabledcontrol-syntax.json"></a>

```
{
  "Type" : "AWS::ControlTower::EnabledControl",
  "Properties" : {
      "[ControlIdentifier](#cfn-controltower-enabledcontrol-controlidentifier)" : String,
      "[TargetIdentifier](#cfn-controltower-enabledcontrol-targetidentifier)" : String
    }
}
```

### YAML<a name="aws-resource-controltower-enabledcontrol-syntax.yaml"></a>

```
Type: AWS::ControlTower::EnabledControl
Properties: 
  [ControlIdentifier](#cfn-controltower-enabledcontrol-controlidentifier): String
  [TargetIdentifier](#cfn-controltower-enabledcontrol-targetidentifier): String
```

## Properties<a name="aws-resource-controltower-enabledcontrol-properties"></a>

`ControlIdentifier`  <a name="cfn-controltower-enabledcontrol-controlidentifier"></a>
The ARN of the control\. Only **Strongly recommended** and **Elective** controls are permitted, with the exception of the **Region deny** guardrail\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetIdentifier`  <a name="cfn-controltower-enabledcontrol-targetidentifier"></a>
The ARN of the organizational unit\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-controltower-enabledcontrol-return-values"></a>

### Ref<a name="aws-resource-controltower-enabledcontrol-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the physical ID of the resource\. The format is of the form `target | control`\. For example:

`arn:aws:organizations::123456789012:ou/o-myorg/ou-my-ouid | arn:aws:controltower:us-west-2::control/AWS-GR_AUTOSCALING_LAUNCH_CONFIG_PUBLIC_IP_DISABLED` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-controltower-enabledcontrol--examples"></a>

### Example<a name="aws-resource-controltower-enabledcontrol--examples--Example"></a>

The following example creates an enabled control named *MyExampleControl* for an OU named *ou\-zzxx\-zzx0zzz2*\.

#### JSON<a name="aws-resource-controltower-enabledcontrol--examples--Example--json"></a>

```
{
    "Resources": {
        "MyExampleControl": {
            "Properties": {
                "ControlIdentifier": "arn:aws:controltower:us-east-2::control/EXAMPLE_NAME",
                 "TargetIdentifier": "arn:aws:organizations::01234567890:ou/o-EXAMPLE/ou-zzxx-zzx0zzz2"
            },
            "Type": "AWS::ControlTower::EnabledControl"
        }
    }
}
```

#### YAML<a name="aws-resource-controltower-enabledcontrol--examples--Example--yaml"></a>

```
Resources:
  MyExampleControl:
    Properties:
      ControlIdentifier: 'arn:aws:controltower:us-east-2::control/EXAMPLE_NAME'
      TargetIdentifier: 'arn:aws:organizations::01234567890:ou/o-EXAMPLE/ou-zzxx-zzx0zzz2'
    Type: 'AWS::ControlTower::EnabledControl'
```