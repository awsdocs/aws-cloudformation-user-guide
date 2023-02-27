# AWS::WAFv2::WebACL BlockAction<a name="aws-properties-wafv2-webacl-blockaction"></a>

Specifies that AWS WAF should block the request and optionally defines additional custom handling for the response to the web request\.

This is used in the context of other settings, for example to specify values for a rule action or a web ACL default action\. 

## Syntax<a name="aws-properties-wafv2-webacl-blockaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-blockaction-syntax.json"></a>

```
{
  "[CustomResponse](#cfn-wafv2-webacl-blockaction-customresponse)" : CustomResponse
}
```

### YAML<a name="aws-properties-wafv2-webacl-blockaction-syntax.yaml"></a>

```
  [CustomResponse](#cfn-wafv2-webacl-blockaction-customresponse): 
    CustomResponse
```

## Properties<a name="aws-properties-wafv2-webacl-blockaction-properties"></a>

`CustomResponse`  <a name="cfn-wafv2-webacl-blockaction-customresponse"></a>
Defines a custom response for the web request\.  
For information about customizing web requests and responses, see [Customizing web requests and responses in AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-custom-request-response.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [CustomResponse](aws-properties-wafv2-webacl-customresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-blockaction--examples"></a>



### Set an block action<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_an_block_action_"></a>

The following shows an example block action specification\. 

#### YAML<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_an_block_action_--yaml"></a>

```
Action:
  Block: {}
```

#### JSON<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_an_block_action_--json"></a>

```
"Action": {
  "Block": {}
}
```

### Set a block action with a custom response setting<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_a_block_action_with_a_custom_response_setting"></a>

The following shows an example block action specification with a custom response setting\. 

#### YAML<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_a_block_action_with_a_custom_response_setting--yaml"></a>

```
Block:
  CustomResponse:
    ResponseCode: 503
    CustomResponseBodyKey: CustomResponseBodyKey1
    ResponseHeaders:
      - Name: BlockActionHeader1Name
        Value: BlockActionHeader1Value
      - Name: BlockActionHeader2Name
        Value: BlockActionHeader2Value
```

#### JSON<a name="aws-properties-wafv2-webacl-blockaction--examples--Set_a_block_action_with_a_custom_response_setting--json"></a>

```
"Block": {
  "CustomResponse": {
    "ResponseCode": 503,
    "CustomResponseBodyKey": "CustomResponseBodyKey1",
    "ResponseHeaders": [
      {
        "Name": "BlockActionHeader1Name",
        "Value": "BlockActionHeader1Value"
      },
      {
        "Name": "BlockActionHeader2Name",
        "Value": "BlockActionHeader2Value"
      }
    ]
  }
}
```