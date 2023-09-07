# AWS::CleanRooms::AnalysisTemplate<a name="aws-resource-cleanrooms-analysistemplate"></a>

Creates a new analysis template\.

## Syntax<a name="aws-resource-cleanrooms-analysistemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cleanrooms-analysistemplate-syntax.json"></a>

```
{
  "Type" : "AWS::CleanRooms::AnalysisTemplate",
  "Properties" : {
      "[AnalysisParameters](#cfn-cleanrooms-analysistemplate-analysisparameters)" : [ AnalysisParameter, ... ],
      "[Description](#cfn-cleanrooms-analysistemplate-description)" : String,
      "[Format](#cfn-cleanrooms-analysistemplate-format)" : String,
      "[MembershipIdentifier](#cfn-cleanrooms-analysistemplate-membershipidentifier)" : String,
      "[Name](#cfn-cleanrooms-analysistemplate-name)" : String,
      "[Source](#cfn-cleanrooms-analysistemplate-source)" : AnalysisSource,
      "[Tags](#cfn-cleanrooms-analysistemplate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cleanrooms-analysistemplate-syntax.yaml"></a>

```
Type: AWS::CleanRooms::AnalysisTemplate
Properties: 
  [AnalysisParameters](#cfn-cleanrooms-analysistemplate-analysisparameters): 
    - AnalysisParameter
  [Description](#cfn-cleanrooms-analysistemplate-description): String
  [Format](#cfn-cleanrooms-analysistemplate-format): String
  [MembershipIdentifier](#cfn-cleanrooms-analysistemplate-membershipidentifier): String
  [Name](#cfn-cleanrooms-analysistemplate-name): String
  [Source](#cfn-cleanrooms-analysistemplate-source): 
    AnalysisSource
  [Tags](#cfn-cleanrooms-analysistemplate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cleanrooms-analysistemplate-properties"></a>

`AnalysisParameters`  <a name="cfn-cleanrooms-analysistemplate-analysisparameters"></a>
The parameters of the analysis template\.  
*Required*: No  
*Type*: List of [AnalysisParameter](aws-properties-cleanrooms-analysistemplate-analysisparameter.md)  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-cleanrooms-analysistemplate-description"></a>
The description of the analysis template\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t\r\n]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-cleanrooms-analysistemplate-format"></a>
The format of the analysis template\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SQL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MembershipIdentifier`  <a name="cfn-cleanrooms-analysistemplate-membershipidentifier"></a>
The identifier for a membership resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `.*[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cleanrooms-analysistemplate-name"></a>
The name of the analysis template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_](([a-zA-Z0-9_ ]+-)*([a-zA-Z0-9_ ]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Source`  <a name="cfn-cleanrooms-analysistemplate-source"></a>
The source of the analysis template\.  
*Required*: Yes  
*Type*: [AnalysisSource](aws-properties-cleanrooms-analysistemplate-analysissource.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cleanrooms-analysistemplate-tags"></a>
An optional label that you can assign to a resource when you create it\. Each tag consists of a key and an optional value, both of which you define\. When you use tagging, you can also use tag\-based access control in IAM policies to control access to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cleanrooms-analysistemplate-return-values"></a>

### Ref<a name="aws-resource-cleanrooms-analysistemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `AnalysisTemplateIdentifier`, such as `a1b2c3d4-5678-90ab-cdef-EXAMPLE2222`\. For example:

 `{ "Ref": "myAnalysisTemplate" }` 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cleanrooms-analysistemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cleanrooms-analysistemplate-return-values-fn--getatt-fn--getatt"></a>

`AnalysisTemplateIdentifier`  <a name="AnalysisTemplateIdentifier-fn::getatt"></a>
Returns the identifier for the analysis template\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE2222`

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the analysis template\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:membership/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111/analysistemplates/a1b2c3d4-5678-90ab-cdef-EXAMPLE2222`

`CollaborationArn`  <a name="CollaborationArn-fn::getatt"></a>
Returns the unique ARN for the analysis template’s associated collaboration\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:collaboration/a1b2c3d4-5678-90ab-cdef-EXAMPLE33333`

`CollaborationIdentifier`  <a name="CollaborationIdentifier-fn::getatt"></a>
Returns the unique ID for the associated collaboration of the analysis template\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE33333`

`MembershipArn`  <a name="MembershipArn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the member who created the analysis template\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:membership/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`Schema`  <a name="Schema-fn::getatt"></a>
Returns the entire [schema object](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cleanrooms-analysistemplate-analysisschema.html)\.

`Schema.ReferencedTables`  <a name="Schema.ReferencedTables-fn::getatt"></a>
Returns the tables referenced in the analysis schema\.  
Example: `[ table1, table2 ]`

## Examples<a name="aws-resource-cleanrooms-analysistemplate--examples"></a>



### Create an analysis template<a name="aws-resource-cleanrooms-analysistemplate--examples--Create_an_analysis_template"></a>

The following example creates an analysis template\.

#### JSON<a name="aws-resource-cleanrooms-analysistemplate--examples--Create_an_analysis_template--json"></a>

```
{
    "ExampleAnalysisTemplate": {
        "Type": "AWS::CleanRooms::AnalysisTemplate",
        "Properties": {
            "MembershipIdentifier": "a1b2c3d4-5678-90ab-cdef-EXAMPLE1111",
            "Name": "exampleAnalysisTemplate",
            "Description": "example description",
            "Source": {
                "Text": "SELECT * FROM cta1 WHERE cta1.column1 > :Param1 AND cta1.column2 like :Param2"
            },
            "Format": "SQL",
            "AnalysisParameters": [
                {
                    "Name": "Param1",
                    "Type": "SMALLINT",
                    "DefaultValue": 1
                },
                {
                    "Name": "Param2",
                    "Type": "CHAR"
                }
            ],
            "Tags": [
                {
                    "Key": "Hello",
                    "Value": "World"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-cleanrooms-analysistemplate--examples--Create_an_analysis_template--yaml"></a>

```
ExampleAnalysisTemplate:
    Type: 'AWS::CleanRooms::AnalysisTemplate'
    Properties:
      MembershipIdentifier: a1b2c3d4-5678-90ab-cdef-EXAMPLE1111
      Name: exampleAnalysisTemplate
      Description: example description
      Source:
        Text: SELECT * FROM cta1 WHERE cta1.column1 > :Param1 AND cta1.column2 like :Param2
      Format: SQL
      AnalysisParameters:
        - Name: Param1
          Type: SMALLINT
          DefaultValue: 1
        - Name: Param2
          Type: CHAR
      Tags:
        - Key: Hello
          Value: World
```