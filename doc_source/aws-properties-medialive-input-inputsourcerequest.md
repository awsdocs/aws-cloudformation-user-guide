# AWS::MediaLive::Input InputSourceRequest<a name="aws-properties-medialive-input-inputsourcerequest"></a>

Settings for for a PULL type input\.

## Syntax<a name="aws-properties-medialive-input-inputsourcerequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-input-inputsourcerequest-syntax.json"></a>

```
{
  "[PasswordParam](#cfn-medialive-input-inputsourcerequest-passwordparam)" : String,
  "[Url](#cfn-medialive-input-inputsourcerequest-url)" : String,
  "[Username](#cfn-medialive-input-inputsourcerequest-username)" : String
}
```

### YAML<a name="aws-properties-medialive-input-inputsourcerequest-syntax.yaml"></a>

```
  [PasswordParam](#cfn-medialive-input-inputsourcerequest-passwordparam): String
  [Url](#cfn-medialive-input-inputsourcerequest-url): String
  [Username](#cfn-medialive-input-inputsourcerequest-username): String
```

## Properties<a name="aws-properties-medialive-input-inputsourcerequest-properties"></a>

`PasswordParam`  <a name="cfn-medialive-input-inputsourcerequest-passwordparam"></a>
The key used to extract the password from EC2 Parameter store\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-medialive-input-inputsourcerequest-url"></a>
This represents the customer's source URL where stream is pulled from\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-medialive-input-inputsourcerequest-username"></a>
The username for the input source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)