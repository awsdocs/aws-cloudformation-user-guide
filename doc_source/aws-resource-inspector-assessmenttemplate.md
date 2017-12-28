# AWS::Inspector::AssessmentTemplate<a name="aws-resource-inspector-assessmenttemplate"></a>

The `AWS::Inspector::AssessmentTemplate` resource creates an Amazon Inspector assessment template \- a resource that contains information about an Amazon Inspector assessment template\.


+ [Syntax](#aws-resource-inspector-assessmenttemplate-syntax)
+ [Properties](#aws-resource-inspector-assessmenttemplate-properties)
+ [Return Values](#aws-resource-inspector-assessmenttemplate-returnvalues)
+ [Examples](#aws-resource-inspector-assessmenttemplate-examples)

## Syntax<a name="aws-resource-inspector-assessmenttemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-inspector-assessmenttemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Inspector::AssessmentTemplate",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-assessmenttargetarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-durationinseconds)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-assessmenttemplatename)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-rulespackagearns)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-userattributesforfindings)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-inspector-assessmenttemplate-syntax.yaml"></a>

```
Type: "AWS::Inspector::AssessmentTemplate"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-assessmenttargetarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-durationinseconds): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-assessmenttemplatename): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-rulespackagearns): 
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-inspector-assessmenttemplate-userattributesforfindings): 
    - Resource Tag
```

## Properties<a name="aws-resource-inspector-assessmenttemplate-properties"></a>

`AssessmentTargetArn`  
The ARN of the assessment target that corresponds to this assessment template\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`DurationInSeconds`  
The duration in seconds specified for this assessment tempate\. The default value is 3600 seconds \(one hour\)\. The maximum value is 86400 seconds \(one day\)\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: Replacement 

`AssessmentTemplateName`  
The name of the assessment template\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`RulesPackageArns`  
The rules packages that are specified for this assessment template\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: Replacement 

`UserAttributesForFindings`  
The user\-defined attributes that are assigned to every generated finding from the assessment run that uses this assessment template\.   
 *Required*: No  
 *Type*: List of   
 *Update requires*: Replacement 

## Return Values<a name="aws-resource-inspector-assessmenttemplate-returnvalues"></a>

### Fn::GetAtt<a name="aws-resource-inspector-assessmenttemplate-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) that specifies the assessment template that is created\. 

For more information about using `Fn::GetAtt`, see Fn::GetAtt\. 

## Examples<a name="aws-resource-inspector-assessmenttemplate-examples"></a>

### Declaring an Amazon Inspector Assessment Template Resource<a name="aws-resource-inspector-assessmenttemplate-example1"></a>

The following example shows how to declare an AWS::Inspector::AssessmentTemplate resource to create an Amazon Inspector assessment template\.

#### JSON<a name="aws-resource-inspector-assessmenttemplate-example1.json"></a>

```
"myassessmenttemplate": {
  "Type": "AWS::Inspector::AssessmentTemplate",
  "Properties": {
      "AssessmentTargetArn" : "arn:aws:inspector:us-west-2:123456789012:target/0-nvgVhaxX",
      "DurationInSeconds" : 180,
	    "AssessmentTemplateName" : "MyAssessmentTemplate",
	    "RulesPackageArns" : [ "arn:aws:inspector:us-west-2:758058086616:rulespackage/0-11B9DBXp" ],
	    "UserAttributesForFindings" : [ 
	       {
            "key": "Example",
            "value": "example"
         }
	]
 }
}
```

#### YAML<a name="aws-resource-inspector-assessmenttemplate-example1.yaml"></a>

```
myassessmenttemplate: 
  Properties: 
    AssessmentTargetArn: "arn:aws:inspector:us-west-2:123456789012:target/0-nvgVhaxX"
    AssessmentTemplateName: MyAssessmentTemplate
    DurationInSeconds: 180
    RulesPackageArns: 
      - "arn:aws:inspector:us-west-2:758058086616:rulespackage/0-11B9DBXp"
    UserAttributesForFindings: 
      - 
        Key: Example
        Value: example
  Type: "AWS::Inspector::AssessmentTemplate"
```