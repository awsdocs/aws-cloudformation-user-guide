# AWS::AmplifyUIBuilder::Form FileUploaderFieldConfig<a name="aws-properties-amplifyuibuilder-form-fileuploaderfieldconfig"></a>

Describes the configuration for the file uploader field\.

## Syntax<a name="aws-properties-amplifyuibuilder-form-fileuploaderfieldconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplifyuibuilder-form-fileuploaderfieldconfig-syntax.json"></a>

```
{
  "[AcceptedFileTypes](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-acceptedfiletypes)" : [ String, ... ],
  "[AccessLevel](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-accesslevel)" : String,
  "[IsResumable](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-isresumable)" : Boolean,
  "[MaxFileCount](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxfilecount)" : Double,
  "[MaxSize](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxsize)" : Double,
  "[ShowThumbnails](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-showthumbnails)" : Boolean
}
```

### YAML<a name="aws-properties-amplifyuibuilder-form-fileuploaderfieldconfig-syntax.yaml"></a>

```
  [AcceptedFileTypes](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-acceptedfiletypes): 
    - String
  [AccessLevel](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-accesslevel): String
  [IsResumable](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-isresumable): Boolean
  [MaxFileCount](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxfilecount): Double
  [MaxSize](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxsize): Double
  [ShowThumbnails](#cfn-amplifyuibuilder-form-fileuploaderfieldconfig-showthumbnails): Boolean
```

## Properties<a name="aws-properties-amplifyuibuilder-form-fileuploaderfieldconfig-properties"></a>

`AcceptedFileTypes`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-acceptedfiletypes"></a>
The file types that are allowed to be uploaded by the file uploader\. Provide this information in an array of strings specifying the valid file extensions\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessLevel`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-accesslevel"></a>
The access level to assign to the uploaded files in the Amazon S3 bucket where they are stored\. The valid values for this property are `private`, `protected`, or `public`\. For detailed information about the permissions associated with each access level, see [File access levels](https://docs.amplify.aws/lib/storage/configureaccess/q/platform/js/) in the *Amplify documentation*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsResumable`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-isresumable"></a>
Allows the file upload operation to be paused and resumed\. The default value is `false`\.  
When `isResumable` is set to `true`, the file uploader uses a multipart upload to break the files into chunks before upload\. The progress of the upload isn't continuous, because the file uploader uploads a chunk at a time\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxFileCount`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxfilecount"></a>
Specifies the maximum number of files that can be selected to upload\. The default value is an unlimited number of files\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-maxsize"></a>
The maximum file size in bytes that the file uploader will accept\. The default value is an unlimited file size\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ShowThumbnails`  <a name="cfn-amplifyuibuilder-form-fileuploaderfieldconfig-showthumbnails"></a>
Specifies whether to display or hide the image preview after selecting a file for upload\. The default value is `true` to display the image preview\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)