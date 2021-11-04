# AWS::Lambda::CodeSigningConfig AllowedPublishers<a name="aws-properties-lambda-codesigningconfig-allowedpublishers"></a>

List of signing profiles that can sign a code package\. 

## Syntax<a name="aws-properties-lambda-codesigningconfig-allowedpublishers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-codesigningconfig-allowedpublishers-syntax.json"></a>

```
{
  "[SigningProfileVersionArns](#cfn-lambda-codesigningconfig-allowedpublishers-signingprofileversionarns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lambda-codesigningconfig-allowedpublishers-syntax.yaml"></a>

```
  [SigningProfileVersionArns](#cfn-lambda-codesigningconfig-allowedpublishers-signingprofileversionarns): 
    - String
```

## Properties<a name="aws-properties-lambda-codesigningconfig-allowedpublishers-properties"></a>

`SigningProfileVersionArns`  <a name="cfn-lambda-codesigningconfig-allowedpublishers-signingprofileversionarns"></a>
The Amazon Resource Name \(ARN\) for each of the signing profiles\. A signing profile defines a trusted user who can sign a code package\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)