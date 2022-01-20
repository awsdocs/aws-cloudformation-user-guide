# AWS::Panorama::ApplicationInstance ManifestPayload<a name="aws-properties-panorama-applicationinstance-manifestpayload"></a>

A application verion's manifest file\. This is a JSON document that has a single key \(`PayloadData`\) where the value is an escaped string representation of the application manifest \(`graph.json`\)\. This file is located in the `graphs` folder in your application source\.

## Syntax<a name="aws-properties-panorama-applicationinstance-manifestpayload-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-panorama-applicationinstance-manifestpayload-syntax.json"></a>

```
{
  "[PayloadData](#cfn-panorama-applicationinstance-manifestpayload-payloaddata)" : String
}
```

### YAML<a name="aws-properties-panorama-applicationinstance-manifestpayload-syntax.yaml"></a>

```
  [PayloadData](#cfn-panorama-applicationinstance-manifestpayload-payloaddata): String
```

## Properties<a name="aws-properties-panorama-applicationinstance-manifestpayload-properties"></a>

`PayloadData`  <a name="cfn-panorama-applicationinstance-manifestpayload-payloaddata"></a>
The application manifest\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `51200`  
*Pattern*: `.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)