# AWS::QuickSight::DataSource CredentialPair<a name="aws-properties-quicksight-datasource-credentialpair"></a>

The combination of user name and password that are used as credentials\.

## Syntax<a name="aws-properties-quicksight-datasource-credentialpair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-credentialpair-syntax.json"></a>

```
{
  "[AlternateDataSourceParameters](#cfn-quicksight-datasource-credentialpair-alternatedatasourceparameters)" : [ DataSourceParameters, ... ],
  "[Password](#cfn-quicksight-datasource-credentialpair-password)" : String,
  "[Username](#cfn-quicksight-datasource-credentialpair-username)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-credentialpair-syntax.yaml"></a>

```
  [AlternateDataSourceParameters](#cfn-quicksight-datasource-credentialpair-alternatedatasourceparameters): 
    - DataSourceParameters
  [Password](#cfn-quicksight-datasource-credentialpair-password): String
  [Username](#cfn-quicksight-datasource-credentialpair-username): String
```

## Properties<a name="aws-properties-quicksight-datasource-credentialpair-properties"></a>

`AlternateDataSourceParameters`  <a name="cfn-quicksight-datasource-credentialpair-alternatedatasourceparameters"></a>
A set of alternate data source parameters that you want to share for these credentials\. The credentials are applied in tandem with the data source parameters when you copy a data source by using a create or update request\. The API operation compares the `DataSourceParameters` structure that's in the request with the structures in the `AlternateDataSourceParameters` allow list\. If the structures are an exact match, the request is allowed to use the new data source with the existing credentials\. If the `AlternateDataSourceParameters` list is null, the `DataSourceParameters` originally used with these `Credentials` is automatically allowed\.  
*Required*: No  
*Type*: List of [DataSourceParameters](aws-properties-quicksight-datasource-datasourceparameters.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-quicksight-datasource-credentialpair-password"></a>
Password\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-quicksight-datasource-credentialpair-username"></a>
User name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)