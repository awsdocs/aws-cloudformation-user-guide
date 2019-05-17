# AWS::SES::ReceiptRule AddHeaderAction<a name="aws-properties-ses-receiptrule-addheaderaction"></a>

When included in a receipt rule, this action adds a header to the received email\.

For information about adding a header using a receipt rule, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-add-header.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-addheaderaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-addheaderaction-syntax.json"></a>

```
{
  "[HeaderName](#cfn-ses-receiptrule-addheaderaction-headername)" : String,
  "[HeaderValue](#cfn-ses-receiptrule-addheaderaction-headervalue)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-addheaderaction-syntax.yaml"></a>

```
  [HeaderName](#cfn-ses-receiptrule-addheaderaction-headername): String
  [HeaderValue](#cfn-ses-receiptrule-addheaderaction-headervalue): String
```

## Properties<a name="aws-properties-ses-receiptrule-addheaderaction-properties"></a>

`HeaderName`  <a name="cfn-ses-receiptrule-addheaderaction-headername"></a>
The name of the header that you want to add to the incoming message\. The name has to contain at least one character, and can contain up to 50 characters\. It can only consist of alphanumeric \(a–z, A–Z, 0–9\) characters and dashes\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderValue`  <a name="cfn-ses-receiptrule-addheaderaction-headervalue"></a>
The content that you want to include in the header\. This value can contain up to 2048 characters\. It can't contain newline \(`\n`\) or carraige return \(`\r`\) characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)