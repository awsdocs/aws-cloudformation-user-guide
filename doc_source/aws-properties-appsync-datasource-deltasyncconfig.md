# AWS::AppSync::DataSource DeltaSyncConfig<a name="aws-properties-appsync-datasource-deltasyncconfig"></a>

Describes a Delta Sync configuration\.

## Syntax<a name="aws-properties-appsync-datasource-deltasyncconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-deltasyncconfig-syntax.json"></a>

```
{
  "[BaseTableTTL](#cfn-appsync-datasource-deltasyncconfig-basetablettl)" : String,
  "[DeltaSyncTableName](#cfn-appsync-datasource-deltasyncconfig-deltasynctablename)" : String,
  "[DeltaSyncTableTTL](#cfn-appsync-datasource-deltasyncconfig-deltasynctablettl)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-deltasyncconfig-syntax.yaml"></a>

```
  [BaseTableTTL](#cfn-appsync-datasource-deltasyncconfig-basetablettl): String
  [DeltaSyncTableName](#cfn-appsync-datasource-deltasyncconfig-deltasynctablename): String
  [DeltaSyncTableTTL](#cfn-appsync-datasource-deltasyncconfig-deltasynctablettl): String
```

## Properties<a name="aws-properties-appsync-datasource-deltasyncconfig-properties"></a>

`BaseTableTTL`  <a name="cfn-appsync-datasource-deltasyncconfig-basetablettl"></a>
The number of minutes an Item is stored in the datasource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeltaSyncTableName`  <a name="cfn-appsync-datasource-deltasyncconfig-deltasynctablename"></a>
The Delta Sync table name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeltaSyncTableTTL`  <a name="cfn-appsync-datasource-deltasyncconfig-deltasynctablettl"></a>
The number of minutes a Delta Sync log entry is stored in the Delta Sync table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)