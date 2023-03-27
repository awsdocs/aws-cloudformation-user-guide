# AWS::ResourceExplorer2::DefaultViewAssociation<a name="aws-resource-resourceexplorer2-defaultviewassociation"></a>

Sets the specified view as the default for the AWS Region in which you call this operation\. If a user makes a search query that doesn't explicitly specify the view to use, Resource Explorer chooses this default view automatically for searches performed in this AWS Region\.

## Syntax<a name="aws-resource-resourceexplorer2-defaultviewassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-resourceexplorer2-defaultviewassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ResourceExplorer2::DefaultViewAssociation",
  "Properties" : {
      "[ViewArn](#cfn-resourceexplorer2-defaultviewassociation-viewarn)" : String
    }
}
```

### YAML<a name="aws-resource-resourceexplorer2-defaultviewassociation-syntax.yaml"></a>

```
Type: AWS::ResourceExplorer2::DefaultViewAssociation
Properties: 
  [ViewArn](#cfn-resourceexplorer2-defaultviewassociation-viewarn): String
```

## Properties<a name="aws-resource-resourceexplorer2-defaultviewassociation-properties"></a>

`ViewArn`  <a name="cfn-resourceexplorer2-defaultviewassociation-viewarn"></a>
The ARN of the view to set as the default for the AWS Region and AWS account in which you call this operation\. The specified view must already exist in the specified Region\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-resourceexplorer2-defaultviewassociation-return-values"></a>

### Ref<a name="aws-resource-resourceexplorer2-defaultviewassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the identity of the principal that the view is now associated with in the specified AWS Region\. For example:

`123456789012`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-resourceexplorer2-defaultviewassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-resourceexplorer2-defaultviewassociation-return-values-fn--getatt-fn--getatt"></a>

`AssociatedAwsPrincipal`  <a name="AssociatedAwsPrincipal-fn::getatt"></a>
The unique identifier of the principal for which the specified view was made the default for the AWS Region that contains the view\. For example:  
`123456789012`

## Examples<a name="aws-resource-resourceexplorer2-defaultviewassociation--examples"></a>

### Designating the default view for the Region<a name="aws-resource-resourceexplorer2-defaultviewassociation--examples--Designating_the_default_view_for_the_Region"></a>

#### JSON<a name="aws-resource-resourceexplorer2-defaultviewassociation--examples--Designating_the_default_view_for_the_Region--json"></a>

```
{
    "Description": "Sample stack template that designates SampleView as the default for its Region",
    "Resources": {
        "SampleDefaultViewAssociation": {
            "Type": "AWS::ResourceExplorer2::DefaultViewAssociation",
            "Properties": {
                "ViewArn": {
                    "Ref": "SampleView"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-resourceexplorer2-defaultviewassociation--examples--Designating_the_default_view_for_the_Region--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: Sample stack template that creates a resource-based policy for SampleView
  SampleDefaultViewAssociation:
    Type: 'AWS::ResourceExplorer2::DefaultViewAssociation'
    Properties:
      ViewArn: !Ref SampleView
```