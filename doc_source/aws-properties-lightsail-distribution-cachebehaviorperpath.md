# AWS::Lightsail::Distribution CacheBehaviorPerPath<a name="aws-properties-lightsail-distribution-cachebehaviorperpath"></a>

`CacheBehaviorPerPath` is a property of the [AWS::Lightsail::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-distribution.html) resource\. It describes the per\-path cache behavior of an Amazon Lightsail content delivery network \(CDN\) distribution\.

Use a per\-path cache behavior to override the default cache behavior of a distribution, or to add an exception to it\. For example, if you set the `CacheBehavior` to `cache`, you can use a per\-path cache behavior to specify a directory, file, or file type that your distribution will cache\. If you don’t want your distribution to cache a specified directory, file, or file type, set the per\-path cache behavior to `dont-cache`\. 

## Syntax<a name="aws-properties-lightsail-distribution-cachebehaviorperpath-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-cachebehaviorperpath-syntax.json"></a>

```
{
  "[Behavior](#cfn-lightsail-distribution-cachebehaviorperpath-behavior)" : String,
  "[Path](#cfn-lightsail-distribution-cachebehaviorperpath-path)" : String
}
```

### YAML<a name="aws-properties-lightsail-distribution-cachebehaviorperpath-syntax.yaml"></a>

```
  [Behavior](#cfn-lightsail-distribution-cachebehaviorperpath-behavior): String
  [Path](#cfn-lightsail-distribution-cachebehaviorperpath-path): String
```

## Properties<a name="aws-properties-lightsail-distribution-cachebehaviorperpath-properties"></a>

`Behavior`  <a name="cfn-lightsail-distribution-cachebehaviorperpath-behavior"></a>
The cache behavior for the specified path\.  
You can specify one of the following per\-path cache behaviors:  
+  ** `cache` ** \- This behavior caches the specified path\. 
+  ** `dont-cache` ** \- This behavior doesn't cache the specified path\. 
*Required*: No  
*Type*: String  
*Allowed values*: `cache | dont-cache`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-lightsail-distribution-cachebehaviorperpath-path"></a>
The path to a directory or file to cache, or not cache\. Use an asterisk symbol to specify wildcard directories \(`path/to/assets/*`\), and file types \(`*.html`, `*jpg`, `*js`\)\. Directories and file paths are case\-sensitive\.  
Examples:  
+ Specify the following to cache all files in the document root of an Apache web server running on a instance\.

   `var/www/html/` 
+ Specify the following file to cache only the index page in the document root of an Apache web server\.

   `var/www/html/index.html` 
+ Specify the following to cache only the \.html files in the document root of an Apache web server\.

   `var/www/html/*.html` 
+ Specify the following to cache only the \.jpg, \.png, and \.gif files in the images sub\-directory of the document root of an Apache web server\.

   `var/www/html/images/*.jpg` 

   `var/www/html/images/*.png` 

   `var/www/html/images/*.gif` 

  Specify the following to cache all files in the images subdirectory of the document root of an Apache web server\.

   `var/www/html/images/` 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)