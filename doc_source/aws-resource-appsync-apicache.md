# AWS::AppSync::ApiCache<a name="aws-resource-appsync-apicache"></a>

The `AWS::AppSync::ApiCache` resource represents the input of a `CreateApiCache` operation\.

## Syntax<a name="aws-resource-appsync-apicache-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-apicache-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::ApiCache",
  "Properties" : {
      "[ApiCachingBehavior](#cfn-appsync-apicache-apicachingbehavior)" : String,
      "[ApiId](#cfn-appsync-apicache-apiid)" : String,
      "[AtRestEncryptionEnabled](#cfn-appsync-apicache-atrestencryptionenabled)" : Boolean,
      "[TransitEncryptionEnabled](#cfn-appsync-apicache-transitencryptionenabled)" : Boolean,
      "[Ttl](#cfn-appsync-apicache-ttl)" : Double,
      "[Type](#cfn-appsync-apicache-type)" : String
    }
}
```

### YAML<a name="aws-resource-appsync-apicache-syntax.yaml"></a>

```
Type: AWS::AppSync::ApiCache
Properties: 
  [ApiCachingBehavior](#cfn-appsync-apicache-apicachingbehavior): String
  [ApiId](#cfn-appsync-apicache-apiid): String
  [AtRestEncryptionEnabled](#cfn-appsync-apicache-atrestencryptionenabled): Boolean
  [TransitEncryptionEnabled](#cfn-appsync-apicache-transitencryptionenabled): Boolean
  [Ttl](#cfn-appsync-apicache-ttl): Double
  [Type](#cfn-appsync-apicache-type): String
```

## Properties<a name="aws-resource-appsync-apicache-properties"></a>

`ApiCachingBehavior`  <a name="cfn-appsync-apicache-apicachingbehavior"></a>
Caching behavior\.  
+  **FULL\_REQUEST\_CACHING**: All requests are fully cached\.
+  **PER\_RESOLVER\_CACHING**: Individual resolvers that you specify are cached\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApiId`  <a name="cfn-appsync-apicache-apiid"></a>
The GraphQL API Id\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AtRestEncryptionEnabled`  <a name="cfn-appsync-apicache-atrestencryptionenabled"></a>
At rest encryption flag for cache\. This setting cannot be updated after creation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitEncryptionEnabled`  <a name="cfn-appsync-apicache-transitencryptionenabled"></a>
Transit encryption flag when connecting to cache\. This setting cannot be updated after creation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ttl`  <a name="cfn-appsync-apicache-ttl"></a>
TTL in seconds for cache entries\.  
Valid values are between 1 and 3600 seconds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-appsync-apicache-type"></a>
The cache instance type\. Valid values are   
+  `SMALL` 
+  `MEDIUM` 
+  `LARGE` 
+  `XLARGE` 
+  `LARGE_2X` 
+  `LARGE_4X` 
+  `LARGE_8X` \(not available in all regions\)
+  `LARGE_12X` 
Historically, instance types were identified by an EC2\-style value\. As of July 2020, this is deprecated, and the generic identifiers above should be used\.  
The following legacy instance types are available, but their use is discouraged:  
+  **T2\_SMALL**: A t2\.small instance type\.
+  **T2\_MEDIUM**: A t2\.medium instance type\.
+  **R4\_LARGE**: A r4\.large instance type\.
+  **R4\_XLARGE**: A r4\.xlarge instance type\.
+  **R4\_2XLARGE**: A r4\.2xlarge instance type\.
+  **R4\_4XLARGE**: A r4\.4xlarge instance type\.
+  **R4\_8XLARGE**: A r4\.8xlarge instance type\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-appsync-apicache--examples"></a>



### ApiCache Creation Example<a name="aws-resource-appsync-apicache--examples--ApiCache_Creation_Example"></a>

The following example creates an ApiCache for your GraphQL API\.

#### YAML<a name="aws-resource-appsync-apicache--examples--ApiCache_Creation_Example--yaml"></a>

```
Parameters: graphQlApiId: Type: String Resources: ApiCache: Type:
            'AWS::AppSync::ApiCache' Properties: ApiId: graphQlApiId Type: T2_SMALL
            ApiCachingBehavior: FULL_REQUEST_CACHING Ttl: 1200 TransitEncryptionEnabled: true
            AtRestEncryptionEnabled: true
```

#### JSON<a name="aws-resource-appsync-apicache--examples--ApiCache_Creation_Example--json"></a>

```
{ "Parameters": { "graphQlApiId": { "Type": "String" } },
            "Resources": { "ApiCache": { "Type": "AWS::AppSync::ApiCache", "Properties": { "ApiId":
            "graphQlApiId", "Type": "T2_SMALL", "ApiCachingBehavior": "FULL_REQUEST_CACHING", "Ttl":
            1200, "TransitEncryptionEnabled": true, "AtRestEncryptionEnabled": true } } }
            }
```