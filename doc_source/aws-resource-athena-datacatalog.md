# AWS::Athena::DataCatalog<a name="aws-resource-athena-datacatalog"></a>

The AWS::Athena::DataCatalog resource specifies an Amazon Athena data catalog, which contains a name, description, type, parameters, and tags\. For more information, see [DataCatalog](https://docs.aws.amazon.com/athena/latest/APIReference/API_DataCatalog.html) in the *Amazon Athena API Reference*\.

## Syntax<a name="aws-resource-athena-datacatalog-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-athena-datacatalog-syntax.json"></a>

```
{
  "Type" : "AWS::Athena::DataCatalog",
  "Properties" : {
      "[Description](#cfn-athena-datacatalog-description)" : String,
      "[Name](#cfn-athena-datacatalog-name)" : String,
      "[Parameters](#cfn-athena-datacatalog-parameters)" : {Key : Value, ...},
      "[Tags](#cfn-athena-datacatalog-tags)" : Tags,
      "[Type](#cfn-athena-datacatalog-type)" : String
    }
}
```

### YAML<a name="aws-resource-athena-datacatalog-syntax.yaml"></a>

```
Type: AWS::Athena::DataCatalog
Properties: 
  [Description](#cfn-athena-datacatalog-description): String
  [Name](#cfn-athena-datacatalog-name): String
  [Parameters](#cfn-athena-datacatalog-parameters): 
    Key : Value
  [Tags](#cfn-athena-datacatalog-tags): 
    Tags
  [Type](#cfn-athena-datacatalog-type): String
```

## Properties<a name="aws-resource-athena-datacatalog-properties"></a>

`Description`  <a name="cfn-athena-datacatalog-description"></a>
A description of the data catalog\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-athena-datacatalog-name"></a>
The name of the data catalog\. The catalog name must be unique for the AWS account and can use a maximum of 128 alphanumeric, underscore, at sign, or hyphen characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-athena-datacatalog-parameters"></a>
Specifies the Lambda function or functions to use for the data catalog\. The mapping used depends on the catalog type\.   
+ The `HIVE` data catalog type uses the following syntax\. The `metadata-function` parameter is required\. `The sdk-version` parameter is optional and defaults to the currently supported version\.

  `metadata-function=lambda_arn, sdk-version=version_number`
+ The `LAMBDA` data catalog type uses one of the following sets of required parameters, but not both\.
  + When one Lambda function processes metadata and another Lambda function reads data, the following syntax is used\. Both parameters are required\.

    `metadata-function=lambda_arn, record-function=lambda_arn`
  + A composite Lambda function that processes both metadata and data uses the following syntax\.

    `function=lambda_arn`
+ The `GLUE` type has no parameters\.
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-athena-datacatalog-tags"></a>
An optional list of comma separated tags \(key\-value pairs\) that are custom attributes for the data catalog\.  
*Required*: No  
*Type*: [Tags](aws-properties-athena-datacatalog-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-athena-datacatalog-type"></a>
The type of data catalog: `LAMBDA` for a federated catalog, `GLUE` for AWS Glue Catalog, or `HIVE` for an external hive metastore\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-athena-datacatalog-return-values"></a>

### Ref<a name="aws-resource-athena-datacatalog-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the data catalog\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-athena-datacatalog--examples"></a>



### Creating an Athena Data Catalog<a name="aws-resource-athena-datacatalog--examples--Creating_an_Athena_Data_Catalog"></a>

The following example template creates a custom Hive data catalog in Athena\.

#### JSON<a name="aws-resource-athena-datacatalog--examples--Creating_an_Athena_Data_Catalog--json"></a>

```
{
    "Resources":{
        "MyAthenaDataCatalog":{
            "Type":"AWS::Athena::DataCatalog",
            "Properties":{
                "Name":"MyCustomDataCatalog",
                "Type":"HIVE",
                "Description":"Custom Hive Catalog Description",
                "Tags":[
                    {
                        "Key":"key1",
                        "Value":"value1"
                    },
                    {
                        "Key":"key2",
                        "Value":"value2"
                    }
                ],
                "Parameters":{
                    "metadata-function":"arn:aws:lambda:us-west-2:111122223333:function:lambdaname"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-athena-datacatalog--examples--Creating_an_Athena_Data_Catalog--yaml"></a>

```
Resources:
  MyAthenaDataCatalog:
    Type: AWS::Athena::DataCatalog
    Properties:
      Name: MyCustomDataCatalog
      Type: HIVE
      Description: Custom Hive Catalog Description
      Tags:
        - Key: "key1"
          Value: "value1"
        - Key: "key2"
          Value: "value2"
      Parameters:
        metadata-function: "arn:aws:lambda:us-west-2:111122223333:function:lambdaname"
```