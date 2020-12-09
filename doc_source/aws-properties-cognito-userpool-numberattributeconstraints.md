# AWS::Cognito::UserPool NumberAttributeConstraints<a name="aws-properties-cognito-userpool-numberattributeconstraints"></a>

The minimum and maximum value of an attribute that is of the number data type\.

## Syntax<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax.json"></a>

```
{
  "[MaxValue](#cfn-cognito-userpool-numberattributeconstraints-maxvalue)" : String,
  "[MinValue](#cfn-cognito-userpool-numberattributeconstraints-minvalue)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-numberattributeconstraints-syntax.yaml"></a>

```
  [MaxValue](#cfn-cognito-userpool-numberattributeconstraints-maxvalue): String
  [MinValue](#cfn-cognito-userpool-numberattributeconstraints-minvalue): String
```

## Properties<a name="aws-properties-cognito-userpool-numberattributeconstraints-properties"></a>

`MaxValue`  <a name="cfn-cognito-userpool-numberattributeconstraints-maxvalue"></a>
The maximum value of an attribute that is of the number data type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinValue`  <a name="cfn-cognito-userpool-numberattributeconstraints-minvalue"></a>
The minimum value of an attribute that is of the number data type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)