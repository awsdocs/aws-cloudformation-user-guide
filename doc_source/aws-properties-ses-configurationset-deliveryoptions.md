# AWS::SES::ConfigurationSet DeliveryOptions<a name="aws-properties-ses-configurationset-deliveryoptions"></a>

Specifies whether messages that use the configuration set are required to use Transport Layer Security \(TLS\)\.

## Syntax<a name="aws-properties-ses-configurationset-deliveryoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-configurationset-deliveryoptions-syntax.json"></a>

```
{
  "[SendingPoolName](#cfn-ses-configurationset-deliveryoptions-sendingpoolname)" : String,
  "[TlsPolicy](#cfn-ses-configurationset-deliveryoptions-tlspolicy)" : String
}
```

### YAML<a name="aws-properties-ses-configurationset-deliveryoptions-syntax.yaml"></a>

```
  [SendingPoolName](#cfn-ses-configurationset-deliveryoptions-sendingpoolname): String
  [TlsPolicy](#cfn-ses-configurationset-deliveryoptions-tlspolicy): String
```

## Properties<a name="aws-properties-ses-configurationset-deliveryoptions-properties"></a>

`SendingPoolName`  <a name="cfn-ses-configurationset-deliveryoptions-sendingpoolname"></a>
The name of the dedicated IP pool to associate with the configuration set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsPolicy`  <a name="cfn-ses-configurationset-deliveryoptions-tlspolicy"></a>
Specifies whether messages that use the configuration set are required to use Transport Layer Security \(TLS\)\. If the value is `REQUIRE`, messages are only delivered if a TLS connection can be established\. If the value is `OPTIONAL`, messages can be delivered in plain text if a TLS connection can't be established\.  
Valid Values: `REQUIRE | OPTIONAL`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)