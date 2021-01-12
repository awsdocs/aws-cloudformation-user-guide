# AWS::Config::StoredQuery<a name="aws-resource-config-storedquery"></a>

Saves a new query or updates an existing saved query\. The QueryName must be unique for a single AWS account and a single AWS Region\. You can create upto 300 queries in a single AWS account and a single AWS Region\. 

## Syntax<a name="aws-resource-config-storedquery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-storedquery-syntax.json"></a>

```
{
  "Type" : "AWS::Config::StoredQuery",
  "Properties" : {
      "[QueryDescription](#cfn-config-storedquery-querydescription)" : String,
      "[QueryExpression](#cfn-config-storedquery-queryexpression)" : String,
      "[QueryName](#cfn-config-storedquery-queryname)" : String,
      "[Tags](#cfn-config-storedquery-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-config-storedquery-syntax.yaml"></a>

```
Type: AWS::Config::StoredQuery
Properties: 
  [QueryDescription](#cfn-config-storedquery-querydescription): String
  [QueryExpression](#cfn-config-storedquery-queryexpression): String
  [QueryName](#cfn-config-storedquery-queryname): String
  [Tags](#cfn-config-storedquery-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-config-storedquery-properties"></a>

`QueryDescription`  <a name="cfn-config-storedquery-querydescription"></a>
A unique description for the query\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryExpression`  <a name="cfn-config-storedquery-queryexpression"></a>
The expression of the query\. For example, `SELECT resourceId, resourceType, supplementaryConfiguration.BucketVersioningConfiguration.status WHERE resourceType = 'AWS::S3::Bucket' AND supplementaryConfiguration.BucketVersioningConfiguration.status = 'Off'`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryName`  <a name="cfn-config-storedquery-queryname"></a>
The name of the query\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[a-zA-Z0-9-_]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-config-storedquery-tags"></a>
An array of tag object\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-storedquery-return-values"></a>

### Ref<a name="aws-resource-config-storedquery-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the stored query\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-config-storedquery-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-config-storedquery-return-values-fn--getatt-fn--getatt"></a>

`QueryArn`  <a name="QueryArn-fn::getatt"></a>
Amazon Resource Name \(ARN\) of the query\. For example, arn:partition:service:region:account\-id:resource\-type/resource\-name/resource\-id\.

`QueryId`  <a name="QueryId-fn::getatt"></a>
The ID of the query\.

## Examples<a name="aws-resource-config-storedquery--examples"></a>



### StoredQuery<a name="aws-resource-config-storedquery--examples--StoredQuery"></a>

The following example saves a stored query

#### JSON<a name="aws-resource-config-storedquery--examples--StoredQuery--json"></a>

```
"StoredQuery": {
    "Type": "AWS::Config::StoredQuery",
    "Properties": {
        "QueryName": "SampleStoredQuery",
        "QueryExpression": "SELECT *",
        "QueryDescription": "A sample query",
        "Tags": [
            {
                "Key": "TagKey",
                "Value": "TagValue"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-config-storedquery--examples--StoredQuery--yaml"></a>

```
StoredQuery:
    Type: AWS::Config::StoredQuery
    Properties:
        QueryName: SampleStoredQuery
        QueryExpression: "SELECT *"
        QueryDescription: "A sample query"
        Tags:
            - Key: "TagKey"
              Value: "TagValue"
```