# AWS::CloudFormation::Authentication<a name="aws-resource-authentication"></a>

Use the `AWS::CloudFormation::Authentication` resource to specify authentication credentials for files or sources that you specify with the [AWS::CloudFormation::Init](aws-resource-init.md) resource\.

To include authentication information for a file or source that you specify with `AWS::CloudFormation::Init`, use the `uris` property if the source is a URI or the `buckets` property if the source is an Amazon S3 bucket\. For more information about files, see [Files](aws-resource-init.md#aws-resource-init-files)\. For more information about sources, see [Sources](aws-resource-init.md#aws-resource-init-sources)\.

You can also specify authentication information for files directly in the `AWS::CloudFormation::Init` resource\. The files key of the resource contains a property named `authentication`\. You can use the `authentication` property to associate authentication information defined in an `AWS::CloudFormation::Authentication` resource directly with a file\.

For files, AWS CloudFormation looks for authentication information in the following order:

1. The `authentication` property of the `AWS::CloudFormation::Init` `files` key\.

1. The `uris` or `buckets` property of the `AWS::CloudFormation::Authentication` resource\.

For sources, AWS CloudFormation looks for authentication information in the `uris` or `buckets` property of the `AWS::CloudFormation::Authentication` resource\.

**Topics**
+ [Syntax](#aws-resource-cloudformation-authentication-syntax)
+ [Properties](#w7739ab1c27c15c15c18c19)
+ [Examples](#aws-resource-authentication-examples)

## Syntax<a name="aws-resource-cloudformation-authentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

You should be aware of the following considerations when using the `AWS::CloudFormation::Authentication` type:
+ Unlike most AWS CloudFormation resources, the `AWS::CloudFormation::Authentication` type does not contain a block called "Properties", but instead contains a list of user\-named blocks, each containing its own authentication properties\.

  Not all properties pertain to each authentication type; see the [type](#cfn-cloudformation-authentication-type) property for more details\.
+ Unlike most AWS CloudFormation resources, property names use lower camel case\.

### JSON<a name="aws-resource-cloudformation-authentication-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::Authentication" {
    "String" : {
      "accessKeyId" : String,
      "buckets" : [ String, ... ],
      "password" : String,
      "secretKey" : String,
      "type" : String,
      "uris" : [ String, ... ],
      "username" : String,
      "roleName" : String
    }
  }
}
```

### YAML<a name="aws-resource-cloudformation-authentication-syntax.yaml"></a>

```
Type: AWS::CloudFormation::Authentication
String:
  accessKeyId: String
  buckets:
    - String
  password: String
  secretKey: String
  type: String
  uris:
    - String
  username: String
  roleName: String
```

## Properties<a name="w7739ab1c27c15c15c18c19"></a>

`accessKeyId`  <a name="cfn-cloudformation-authentication-accesskeyid"></a>
Specifies the access key ID for S3 authentication\.  
*Required*: Conditional\. Can be specified only if the `type` property is set to `"S3"`\.  
*Type*: String

`buckets`  <a name="cfn-cloudformation-authentication-buckets"></a>
A comma\-delimited list of Amazon S3 buckets to be associated with the S3 authentication credentials\.  
*Required*: Conditional\. Can be specified only if the `type` property is set to `"S3"`\.  
*Type*: List of String values

`password`  <a name="cfn-cloudformation-authentication-password"></a>
Specifies the password for basic authentication\.  
*Required*: Conditional\. Can be specified only if the type property is set to `"basic"`\.  
*Type*: String

`secretKey`  <a name="cfn-cloudformation-authentication-secretkey"></a>
Specifies the secret key for S3 authentication\.  
*Required*: Conditional\. Can be specified only if the `type` property is set to `"S3"`\.  
*Type*: String

`type`  <a name="cfn-cloudformation-authentication-type"></a>
Specifies whether the authentication scheme uses a user name and password \("basic"\) or an access key ID and secret key \("S3"\)\.  
If you specify `"basic"`, specify the `username`, `password`, and `uris` properties\.  
If you specify `"S3"`, specify the `accessKeyId`, `secretKey`, and `buckets` \(optional\) properties\.  
*Required*: Yes  
*Type*: String Valid values are "basic" or "S3"

`uris`  <a name="cfn-cloudformation-authentication-uris"></a>
A comma\-delimited list of URIs to be associated with the basic authentication credentials\. The authorization applies to the specified URIs and any more specific URI\. For example, if you specify `http://www.example.com`, the authorization will also apply to `http://www.example.com/test`\.  
*Required*: Conditional\. Can be specified only if the `type` property is set to `"basic"`\.  
*Type*: List of String values

`username`  <a name="cfn-cloudformation-authentication-username"></a>
Specifies the user name for basic authentication\.  
*Required*: Conditional\. Can be specified only if the type property is set to `"basic"`\.  
*Type*: String

`roleName`  <a name="cfn-cloudformation-authentication-rolename"></a>
Describes the role for role\-based authentication\.   
This role must be contained within the instance profile that is attached to the EC2 instance\. An instance profile can only contain one IAM role\.
*Required*: Conditional\. Can be specified only if the `type` property is set to `"S3"`\.  
*Type*: String\.

## Examples<a name="aws-resource-authentication-examples"></a>

**Note**  
Unlike most resources, the `AWS::CloudFormation::Authentication` type defines a list of user\-named blocks, each of which contains authentication properties that use lower camel case naming\.

### EC2 web server authentication<a name="w7739ab1c27c15c15c18c21b4"></a>

This template snippet shows how to get a file from a private S3 bucket within an EC2 instance\. The credentials used for authentication are defined in the `AWS::CloudFormation::Authentication` resource, and referenced by the `AWS::CloudFormation::Init` resource in the *files* section\.

#### JSON<a name="aws-resource-cloudformation-authentication-example1.json"></a>

```
"WebServer": {
   "Type": "AWS::EC2::Instance",
   "DependsOn" : "BucketPolicy",
   "Metadata" : {
      "AWS::CloudFormation::Init" : {
         "config" : {
            "packages" : { "yum" : { "httpd" : [] } },
            "files" : {
               "/var/www/html/index.html" : {
                  "source" : {
                     "Fn::Join" : [
                        "", [ "http://s3.amazonaws.com/", { "Ref" : "BucketName" }, "/index.html" ]
                     ]
                  },
                  "mode"   : "000400",
                  "owner"  : "apache",
                  "group"  : "apache",
                  "authentication" : "S3AccessCreds"
               }
            },
            "services" : {
               "sysvinit" : {
                  "httpd" : { "enabled" : "true", "ensureRunning" : "true" }
               }
            }
         }
      },
      "AWS::CloudFormation::Authentication" : {
         "S3AccessCreds" : {
            "type" : "S3",
            "accessKeyId" : { "Ref" : "CfnKeys" },
            "secretKey" : { "Fn::GetAtt": [ "CfnKeys", "SecretAccessKey" ] }
         }
      }
   },
   "Properties": {
      EC2 Resource Properties ...
   }
}
```

#### YAML<a name="aws-resource-cloudformation-authentication-example1.yaml"></a>

```
WebServer: 
  Type: AWS::EC2::Instance
  DependsOn: "BucketPolicy"
  Metadata: 
    AWS::CloudFormation::Init: 
      config: 
        packages: 
          yum: 
            httpd: []
        files: 
          /var/www/html/index.html: 
            source: 
              Fn::Join: 
                - ""
                - 
                  - "http://s3.amazonaws.com/"
                  - Ref: "BucketName"
                  - "/index.html"
            mode: "000400"
            owner: "apache"
            group: "apache"
            authentication: "S3AccessCreds"
        services: 
          sysvinit: 
            httpd: 
              enabled: "true"
              ensureRunning: "true"
    AWS::CloudFormation::Authentication: 
      S3AccessCreds: 
        type: "S3"
        accessKeyId: 
          Ref: "CfnKeys"
        secretKey: 
          Fn::GetAtt: 
            - "CfnKeys"
            - "SecretAccessKey"
Properties: 
  EC2 Resource Properties ...
```

### Specifying both basic and S3 authentication<a name="w7739ab1c27c15c15c18c21b6"></a>

The following example template snippet includes both *basic* and *S3* authentication types\.

#### JSON<a name="aws-resource-cloudformation-authentication-example2.json"></a>

```
"AWS::CloudFormation::Authentication" : {
   "testBasic" : {
      "type" : "basic",
      "username" : { "Ref" : "UserName" },
      "password" : { "Ref" : "Password" },
      "uris" : [ "example.com/test" ]
   },
   "testS3" : {
      "type" : "S3",
      "accessKeyId" : { "Ref" : "AccessKeyID" },
      "secretKey" : { "Ref" : "SecretAccessKeyID" },
      "buckets" : [ "DOC-EXAMPLE-BUCKET1" ]
   }
}
```

#### YAML<a name="aws-resource-cloudformation-authentication-example2.yaml"></a>

```
AWS::CloudFormation::Authentication: 
  testBasic: 
    type: "basic"
    username: 
      Ref: "UserName"
    password: 
      Ref: "Password"
    uris: 
      - "example.com/test"
  testS3: 
    type: "S3"
    accessKeyId: 
      Ref: "AccessKeyID"
    secretKey: 
      Ref: "SecretAccessKeyID"
    buckets: 
      - "myawsbucket"
```

### IAM roles<a name="w7739ab1c27c15c15c18c21b8"></a>

The following example shows how to use IAM roles:
+ `myRole` is an [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html) resource\.
+ The Amazon EC2 instance that runs `cfn-init` is associated with `myRole` through an instance profile\.
+ The example specifies the authentication by using the `buckets` property, like in Amazon S3 authentication\. You can also specify authentication by name\.

#### JSON<a name="aws-resource-cloudformation-authentication-example3.json"></a>

```
"AWS::CloudFormation::Authentication": {
    "rolebased" : {
        "type": "S3",
        "buckets": [ "myBucket" ],
        "roleName": { "Ref": "myRole" }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-authentication-example3.yaml"></a>

```
AWS::CloudFormation::Authentication: 
  rolebased: 
    type: "S3"
    buckets: 
      - "myBucket"
    roleName: 
      Ref: "myRole"
```