# AWS::WAFv2::WebACL RequestInspection<a name="aws-properties-wafv2-webacl-requestinspection"></a>

The criteria for inspecting login requests, used by the ATP rule group to validate credentials usage\. 

This is part of the `AWSManagedRulesATPRuleSet` configuration in `ManagedRuleGroupConfig`\.

In these settings, you specify how your application accepts login attempts by providing the request payload type and the names of the fields within the request body where the username and password are provided\. 

## Syntax<a name="aws-properties-wafv2-webacl-requestinspection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-requestinspection-syntax.json"></a>

```
{
  "[PasswordField](#cfn-wafv2-webacl-requestinspection-passwordfield)" : FieldIdentifier,
  "[PayloadType](#cfn-wafv2-webacl-requestinspection-payloadtype)" : String,
  "[UsernameField](#cfn-wafv2-webacl-requestinspection-usernamefield)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-wafv2-webacl-requestinspection-syntax.yaml"></a>

```
  [PasswordField](#cfn-wafv2-webacl-requestinspection-passwordfield): 
    FieldIdentifier
  [PayloadType](#cfn-wafv2-webacl-requestinspection-payloadtype): String
  [UsernameField](#cfn-wafv2-webacl-requestinspection-usernamefield): 
    FieldIdentifier
```

## Properties<a name="aws-properties-wafv2-webacl-requestinspection-properties"></a>

`PasswordField`  <a name="cfn-wafv2-webacl-requestinspection-passwordfield"></a>
Details about your login page password field\.   
How you specify this depends on the payload type\.  
+ For JSON payloads, specify the field name in JSON pointer syntax\. For information about the JSON Pointer syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\. 

  For example, for the JSON payload `{ "login": { "username": "THE_USERNAME", "password": "THE_PASSWORD" } }`, the username field specification is `/login/username` and the password field specification is `/login/password`\.
+ For form encoded payload types, use the HTML form names\.

  For example, for an HTML form with input elements named `username1` and `password1`, the username field specification is `username1` and the password field specification is `password1`\.
*Required*: Yes  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadType`  <a name="cfn-wafv2-webacl-requestinspection-payloadtype"></a>
The payload type for your login endpoint, either JSON or form encoded\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORM_ENCODED | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameField`  <a name="cfn-wafv2-webacl-requestinspection-usernamefield"></a>
Details about your login page username field\.   
How you specify this depends on the payload type\.  
+ For JSON payloads, specify the field name in JSON pointer syntax\. For information about the JSON Pointer syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\. 

  For example, for the JSON payload `{ "login": { "username": "THE_USERNAME", "password": "THE_PASSWORD" } }`, the username field specification is `/login/username` and the password field specification is `/login/password`\.
+ For form encoded payload types, use the HTML form names\.

  For example, for an HTML form with input elements named `username1` and `password1`, the username field specification is `username1` and the password field specification is `password1`\.
*Required*: Yes  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-requestinspection--examples"></a>



### Configure the request inspection fields for a JSON payload<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_JSON_payload_"></a>

The following shows an example `RequestInspection` for a JSON payload type\. 

#### YAML<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_JSON_payload_--yaml"></a>

```
RequestInspection:
  PayloadType: JSON
  UsernameField:
    Identifier: /form/username
  PasswordField:
    Identifier: /form/password
```

#### JSON<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_JSON_payload_--json"></a>

```
"RequestInspection": {
      "PayloadType": "JSON",
      "UsernameField": {
          "Identifier": "/form/username"
      },
      "PasswordField": {
          "Identifier": "/form/password"
      }
  }
```

### Configure the request inspection fields for a form encoded payload<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_form_encoded_payload_"></a>

The following shows an example `RequestInspection` for a form encoded payload type\. 

#### YAML<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_form_encoded_payload_--yaml"></a>

```
RequestInspection:
  PayloadType: FORM_ENCODED
  UsernameField:
    Identifier: username
  PasswordField:
    Identifier: password
```

#### JSON<a name="aws-properties-wafv2-webacl-requestinspection--examples--Configure_the_request_inspection_fields_for_a_form_encoded_payload_--json"></a>

```
"RequestInspection": {
      "PayloadType": "FORM_ENCODED",
      "UsernameField": {
          "Identifier": "username"
      },
      "PasswordField": {
          "Identifier": "password"
      }
  }
```