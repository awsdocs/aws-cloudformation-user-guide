# AWS::PinpointEmail::ConfigurationSet DeliveryOptions<a name="aws-properties-pinpointemail-configurationset-deliveryoptions"></a>

Used to associate a configuration set with a dedicated IP pool\.

## Syntax<a name="aws-properties-pinpointemail-configurationset-deliveryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-configurationset-deliveryoptions-syntax.json"></a>

```
{
  "[SendingPoolName](#cfn-pinpointemail-configurationset-deliveryoptions-sendingpoolname)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-configurationset-deliveryoptions-syntax.yaml"></a>

```
  [SendingPoolName](#cfn-pinpointemail-configurationset-deliveryoptions-sendingpoolname): String
```

## Properties<a name="aws-properties-pinpointemail-configurationset-deliveryoptions-properties"></a>

`SendingPoolName`  <a name="cfn-pinpointemail-configurationset-deliveryoptions-sendingpoolname"></a>
The name of the dedicated IP pool that you want to associate with the configuration set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
