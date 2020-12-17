# Format version<a name="format-version-structure"></a>

The `AWSTemplateFormatVersion` section \(optional\) identifies the capabilities of the template\. The latest template format version is `2010-09-09` and is currently the only valid value\.

**Note**  
The template format version is not the same as the API or WSDL version\. The template format version can change independently of the API and WSDL versions\.

The value for the template format version declaration must be a literal string\. You cannot use a parameter or function to specify the template format version\. If you don't specify a value, AWS CloudFormation assumes the latest template format version\. The following snippet is an example of a valid template format version declaration:

## JSON<a name="format-version-structure-example.json"></a>

```
"AWSTemplateFormatVersion" : "2010-09-09"
```

## YAML<a name="format-version-structure-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
```