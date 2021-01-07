# AWS::MediaLive::Channel HlsGroupSettings<a name="aws-properties-medialive-channel-hlsgroupsettings"></a>

The settings for an HLS output group\.

The parent of this entity is OutputGroupSettings\.

## Syntax<a name="aws-properties-medialive-channel-hlsgroupsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-hlsgroupsettings-syntax.json"></a>

```
{
  "[AdMarkers](#cfn-medialive-channel-hlsgroupsettings-admarkers)" : [ String, ... ],
  "[BaseUrlContent](#cfn-medialive-channel-hlsgroupsettings-baseurlcontent)" : String,
  "[BaseUrlContent1](#cfn-medialive-channel-hlsgroupsettings-baseurlcontent1)" : String,
  "[BaseUrlManifest](#cfn-medialive-channel-hlsgroupsettings-baseurlmanifest)" : String,
  "[BaseUrlManifest1](#cfn-medialive-channel-hlsgroupsettings-baseurlmanifest1)" : String,
  "[CaptionLanguageMappings](#cfn-medialive-channel-hlsgroupsettings-captionlanguagemappings)" : [ CaptionLanguageMapping, ... ],
  "[CaptionLanguageSetting](#cfn-medialive-channel-hlsgroupsettings-captionlanguagesetting)" : String,
  "[ClientCache](#cfn-medialive-channel-hlsgroupsettings-clientcache)" : String,
  "[CodecSpecification](#cfn-medialive-channel-hlsgroupsettings-codecspecification)" : String,
  "[ConstantIv](#cfn-medialive-channel-hlsgroupsettings-constantiv)" : String,
  "[Destination](#cfn-medialive-channel-hlsgroupsettings-destination)" : OutputLocationRef,
  "[DirectoryStructure](#cfn-medialive-channel-hlsgroupsettings-directorystructure)" : String,
  "[EncryptionType](#cfn-medialive-channel-hlsgroupsettings-encryptiontype)" : String,
  "[HlsCdnSettings](#cfn-medialive-channel-hlsgroupsettings-hlscdnsettings)" : HlsCdnSettings,
  "[HlsId3SegmentTagging](#cfn-medialive-channel-hlsgroupsettings-hlsid3segmenttagging)" : String,
  "[IFrameOnlyPlaylists](#cfn-medialive-channel-hlsgroupsettings-iframeonlyplaylists)" : String,
  "[IndexNSegments](#cfn-medialive-channel-hlsgroupsettings-indexnsegments)" : Integer,
  "[InputLossAction](#cfn-medialive-channel-hlsgroupsettings-inputlossaction)" : String,
  "[IvInManifest](#cfn-medialive-channel-hlsgroupsettings-ivinmanifest)" : String,
  "[IvSource](#cfn-medialive-channel-hlsgroupsettings-ivsource)" : String,
  "[KeepSegments](#cfn-medialive-channel-hlsgroupsettings-keepsegments)" : Integer,
  "[KeyFormat](#cfn-medialive-channel-hlsgroupsettings-keyformat)" : String,
  "[KeyFormatVersions](#cfn-medialive-channel-hlsgroupsettings-keyformatversions)" : String,
  "[KeyProviderSettings](#cfn-medialive-channel-hlsgroupsettings-keyprovidersettings)" : KeyProviderSettings,
  "[ManifestCompression](#cfn-medialive-channel-hlsgroupsettings-manifestcompression)" : String,
  "[ManifestDurationFormat](#cfn-medialive-channel-hlsgroupsettings-manifestdurationformat)" : String,
  "[MinSegmentLength](#cfn-medialive-channel-hlsgroupsettings-minsegmentlength)" : Integer,
  "[Mode](#cfn-medialive-channel-hlsgroupsettings-mode)" : String,
  "[OutputSelection](#cfn-medialive-channel-hlsgroupsettings-outputselection)" : String,
  "[ProgramDateTime](#cfn-medialive-channel-hlsgroupsettings-programdatetime)" : String,
  "[ProgramDateTimePeriod](#cfn-medialive-channel-hlsgroupsettings-programdatetimeperiod)" : Integer,
  "[RedundantManifest](#cfn-medialive-channel-hlsgroupsettings-redundantmanifest)" : String,
  "[SegmentationMode](#cfn-medialive-channel-hlsgroupsettings-segmentationmode)" : String,
  "[SegmentLength](#cfn-medialive-channel-hlsgroupsettings-segmentlength)" : Integer,
  "[SegmentsPerSubdirectory](#cfn-medialive-channel-hlsgroupsettings-segmentspersubdirectory)" : Integer,
  "[StreamInfResolution](#cfn-medialive-channel-hlsgroupsettings-streaminfresolution)" : String,
  "[TimedMetadataId3Frame](#cfn-medialive-channel-hlsgroupsettings-timedmetadataid3frame)" : String,
  "[TimedMetadataId3Period](#cfn-medialive-channel-hlsgroupsettings-timedmetadataid3period)" : Integer,
  "[TimestampDeltaMilliseconds](#cfn-medialive-channel-hlsgroupsettings-timestampdeltamilliseconds)" : Integer,
  "[TsFileMode](#cfn-medialive-channel-hlsgroupsettings-tsfilemode)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-hlsgroupsettings-syntax.yaml"></a>

```
  [AdMarkers](#cfn-medialive-channel-hlsgroupsettings-admarkers): 
    - String
  [BaseUrlContent](#cfn-medialive-channel-hlsgroupsettings-baseurlcontent): String
  [BaseUrlContent1](#cfn-medialive-channel-hlsgroupsettings-baseurlcontent1): String
  [BaseUrlManifest](#cfn-medialive-channel-hlsgroupsettings-baseurlmanifest): String
  [BaseUrlManifest1](#cfn-medialive-channel-hlsgroupsettings-baseurlmanifest1): String
  [CaptionLanguageMappings](#cfn-medialive-channel-hlsgroupsettings-captionlanguagemappings): 
    - CaptionLanguageMapping
  [CaptionLanguageSetting](#cfn-medialive-channel-hlsgroupsettings-captionlanguagesetting): String
  [ClientCache](#cfn-medialive-channel-hlsgroupsettings-clientcache): String
  [CodecSpecification](#cfn-medialive-channel-hlsgroupsettings-codecspecification): String
  [ConstantIv](#cfn-medialive-channel-hlsgroupsettings-constantiv): String
  [Destination](#cfn-medialive-channel-hlsgroupsettings-destination): 
    OutputLocationRef
  [DirectoryStructure](#cfn-medialive-channel-hlsgroupsettings-directorystructure): String
  [EncryptionType](#cfn-medialive-channel-hlsgroupsettings-encryptiontype): String
  [HlsCdnSettings](#cfn-medialive-channel-hlsgroupsettings-hlscdnsettings): 
    HlsCdnSettings
  [HlsId3SegmentTagging](#cfn-medialive-channel-hlsgroupsettings-hlsid3segmenttagging): String
  [IFrameOnlyPlaylists](#cfn-medialive-channel-hlsgroupsettings-iframeonlyplaylists): String
  [IndexNSegments](#cfn-medialive-channel-hlsgroupsettings-indexnsegments): Integer
  [InputLossAction](#cfn-medialive-channel-hlsgroupsettings-inputlossaction): String
  [IvInManifest](#cfn-medialive-channel-hlsgroupsettings-ivinmanifest): String
  [IvSource](#cfn-medialive-channel-hlsgroupsettings-ivsource): String
  [KeepSegments](#cfn-medialive-channel-hlsgroupsettings-keepsegments): Integer
  [KeyFormat](#cfn-medialive-channel-hlsgroupsettings-keyformat): String
  [KeyFormatVersions](#cfn-medialive-channel-hlsgroupsettings-keyformatversions): String
  [KeyProviderSettings](#cfn-medialive-channel-hlsgroupsettings-keyprovidersettings): 
    KeyProviderSettings
  [ManifestCompression](#cfn-medialive-channel-hlsgroupsettings-manifestcompression): String
  [ManifestDurationFormat](#cfn-medialive-channel-hlsgroupsettings-manifestdurationformat): String
  [MinSegmentLength](#cfn-medialive-channel-hlsgroupsettings-minsegmentlength): Integer
  [Mode](#cfn-medialive-channel-hlsgroupsettings-mode): String
  [OutputSelection](#cfn-medialive-channel-hlsgroupsettings-outputselection): String
  [ProgramDateTime](#cfn-medialive-channel-hlsgroupsettings-programdatetime): String
  [ProgramDateTimePeriod](#cfn-medialive-channel-hlsgroupsettings-programdatetimeperiod): Integer
  [RedundantManifest](#cfn-medialive-channel-hlsgroupsettings-redundantmanifest): String
  [SegmentationMode](#cfn-medialive-channel-hlsgroupsettings-segmentationmode): String
  [SegmentLength](#cfn-medialive-channel-hlsgroupsettings-segmentlength): Integer
  [SegmentsPerSubdirectory](#cfn-medialive-channel-hlsgroupsettings-segmentspersubdirectory): Integer
  [StreamInfResolution](#cfn-medialive-channel-hlsgroupsettings-streaminfresolution): String
  [TimedMetadataId3Frame](#cfn-medialive-channel-hlsgroupsettings-timedmetadataid3frame): String
  [TimedMetadataId3Period](#cfn-medialive-channel-hlsgroupsettings-timedmetadataid3period): Integer
  [TimestampDeltaMilliseconds](#cfn-medialive-channel-hlsgroupsettings-timestampdeltamilliseconds): Integer
  [TsFileMode](#cfn-medialive-channel-hlsgroupsettings-tsfilemode): String
```

## Properties<a name="aws-properties-medialive-channel-hlsgroupsettings-properties"></a>

`AdMarkers`  <a name="cfn-medialive-channel-hlsgroupsettings-admarkers"></a>
Chooses one or more ad marker types to pass SCTE35 signals through to this group of Apple HLS outputs\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseUrlContent`  <a name="cfn-medialive-channel-hlsgroupsettings-baseurlcontent"></a>
A partial URI prefix that will be prepended to each output in the media \.m3u8 file\. The partial URI prefix can be used if the base manifest is delivered from a different URL than the main \.m3u8 file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseUrlContent1`  <a name="cfn-medialive-channel-hlsgroupsettings-baseurlcontent1"></a>
Optional\. One value per output group\. This field is required only if you are completing Base URL content A, and the downstream system has notified you that the media files for pipeline 1 of all outputs are in a location different from the media files for pipeline 0\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseUrlManifest`  <a name="cfn-medialive-channel-hlsgroupsettings-baseurlmanifest"></a>
A partial URI prefix that will be prepended to each output in the media \.m3u8 file\. The partial URI prefix can be used if the base manifest is delivered from a different URL than the main \.m3u8 file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BaseUrlManifest1`  <a name="cfn-medialive-channel-hlsgroupsettings-baseurlmanifest1"></a>
Optional\. One value per output group\. Complete this field only if you are completing Base URL manifest A, and the downstream system has notified you that the child manifest files for pipeline 1 of all outputs are in a location different from the child manifest files for pipeline 0\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionLanguageMappings`  <a name="cfn-medialive-channel-hlsgroupsettings-captionlanguagemappings"></a>
A mapping of up to 4 captions channels to captions languages\. This is meaningful only if captionLanguageSetting is set to "insert\."  
*Required*: No  
*Type*: List of [CaptionLanguageMapping](aws-properties-medialive-channel-captionlanguagemapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptionLanguageSetting`  <a name="cfn-medialive-channel-hlsgroupsettings-captionlanguagesetting"></a>
Applies only to 608 embedded output captions\. Insert: Include CLOSED\-CAPTIONS lines in the manifest\. Specify at least one language in the CC1 Language Code field\. One CLOSED\-CAPTION line is added for each Language Code that you specify\. Make sure to specify the languages in the order in which they appear in the original source \(if the source is embedded format\) or the order of the captions selectors \(if the source is other than embedded\)\. Otherwise, languages in the manifest will not match properly with the output captions\. None: Include the CLOSED\-CAPTIONS=NONE line in the manifest\. Omit: Omit any CLOSED\-CAPTIONS line from the manifest\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCache`  <a name="cfn-medialive-channel-hlsgroupsettings-clientcache"></a>
When set to "disabled," sets the \#EXT\-X\-ALLOW\-CACHE:no tag in the manifest, which prevents clients from saving media segments for later replay\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodecSpecification`  <a name="cfn-medialive-channel-hlsgroupsettings-codecspecification"></a>
The specification to use \(RFC\-6381 or the default RFC\-4281\) during m3u8 playlist generation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConstantIv`  <a name="cfn-medialive-channel-hlsgroupsettings-constantiv"></a>
Used with encryptionType\. This is a 128\-bit, 16\-byte hex value that is represented by a 32\-character text string\. If ivSource is set to "explicit," this parameter is required and is used as the IV for encryption\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-medialive-channel-hlsgroupsettings-destination"></a>
A directory or HTTP destination for the HLS segments, manifest files, and encryption keys \(if enabled\)\.  
*Required*: No  
*Type*: [OutputLocationRef](aws-properties-medialive-channel-outputlocationref.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DirectoryStructure`  <a name="cfn-medialive-channel-hlsgroupsettings-directorystructure"></a>
Places segments in subdirectories\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionType`  <a name="cfn-medialive-channel-hlsgroupsettings-encryptiontype"></a>
Encrypts the segments with the specified encryption scheme\. Exclude this parameter if you don't want encryption\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsCdnSettings`  <a name="cfn-medialive-channel-hlsgroupsettings-hlscdnsettings"></a>
The parameters that control interactions with the CDN\.  
*Required*: No  
*Type*: [HlsCdnSettings](aws-properties-medialive-channel-hlscdnsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HlsId3SegmentTagging`  <a name="cfn-medialive-channel-hlsgroupsettings-hlsid3segmenttagging"></a>
State of HLS ID3 Segment Tagging  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IFrameOnlyPlaylists`  <a name="cfn-medialive-channel-hlsgroupsettings-iframeonlyplaylists"></a>
DISABLED: Don't create an I\-frame\-only manifest, but do create the master and media manifests \(according to the Output Selection field\)\. STANDARD: Create an I\-frame\-only manifest for each output that contains video, as well as the other manifests \(according to the Output Selection field\)\. The I\-frame manifest contains a \#EXT\-X\-I\-FRAMES\-ONLY tag to indicate it is I\-frame only, and one or more \#EXT\-X\-BYTERANGE entries identifying the I\-frame position\. For example, \#EXT\-X\-BYTERANGE:160364@1461888"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexNSegments`  <a name="cfn-medialive-channel-hlsgroupsettings-indexnsegments"></a>
Applies only if the Mode field is LIVE\. Specifies the maximum number of segments in the media manifest file\. After this maximum, older segments are removed from the media manifest\. This number must be less than or equal to the Keep Segments field\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossAction`  <a name="cfn-medialive-channel-hlsgroupsettings-inputlossaction"></a>
A parameter that controls output group behavior on an input loss\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IvInManifest`  <a name="cfn-medialive-channel-hlsgroupsettings-ivinmanifest"></a>
Used with encryptionType\. The IV \(initialization vector\) is a 128\-bit number used in conjunction with the key for encrypting blocks\. If set to "include," the IV is listed in the manifest\. Otherwise, the IV is not in the manifest\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IvSource`  <a name="cfn-medialive-channel-hlsgroupsettings-ivsource"></a>
Used with encryptionType\. The IV \(initialization vector\) is a 128\-bit number used in conjunction with the key for encrypting blocks\. If this setting is "followsSegmentNumber," it causes the IV to change every segment \(to match the segment number\)\. If this is set to "explicit," you must enter a constantIv value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeepSegments`  <a name="cfn-medialive-channel-hlsgroupsettings-keepsegments"></a>
Applies only if the Mode field is LIVE\. Specifies the number of media segments \(\.ts files\) to retain in the destination directory\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyFormat`  <a name="cfn-medialive-channel-hlsgroupsettings-keyformat"></a>
Specifies how the key is represented in the resource identified by the URI\. If the parameter is absent, an implicit value of "identity" is used\. A reverse DNS string can also be specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyFormatVersions`  <a name="cfn-medialive-channel-hlsgroupsettings-keyformatversions"></a>
Either a single positive integer version value or a slash\-delimited list of version values \(1/2/3\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyProviderSettings`  <a name="cfn-medialive-channel-hlsgroupsettings-keyprovidersettings"></a>
The key provider settings\.  
*Required*: No  
*Type*: [KeyProviderSettings](aws-properties-medialive-channel-keyprovidersettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestCompression`  <a name="cfn-medialive-channel-hlsgroupsettings-manifestcompression"></a>
When set to gzip, compresses HLS playlist\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManifestDurationFormat`  <a name="cfn-medialive-channel-hlsgroupsettings-manifestdurationformat"></a>
Indicates whether the output manifest should use a floating point or integer values for segment duration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSegmentLength`  <a name="cfn-medialive-channel-hlsgroupsettings-minsegmentlength"></a>
When set, minimumSegmentLength is enforced by looking ahead and back within the specified range for a nearby avail and extending the segment size if needed\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-medialive-channel-hlsgroupsettings-mode"></a>
If "vod," all segments are indexed and kept permanently in the destination and manifest\. If "live," only the number segments specified in keepSegments and indexNSegments are kept\. Newer segments replace older segments, which might prevent players from rewinding all the way to the beginning of the channel\. VOD mode uses HLS EXT\-X\-PLAYLIST\-TYPE of EVENT while the channel is running, converting it to a "VOD" type manifest on completion of the stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSelection`  <a name="cfn-medialive-channel-hlsgroupsettings-outputselection"></a>
MANIFESTSANDSEGMENTS: Generates manifests \(the master manifest, if applicable, and media manifests\) for this output group\. SEGMENTSONLY: Doesn't generate any manifests for this output group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTime`  <a name="cfn-medialive-channel-hlsgroupsettings-programdatetime"></a>
Includes or excludes the EXT\-X\-PROGRAM\-DATE\-TIME tag in \.m3u8 manifest files\. The value is calculated as follows: Either the program date and time are initialized using the input timecode source, or the time is initialized using the input timecode source and the date is initialized using the timestampOffset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgramDateTimePeriod`  <a name="cfn-medialive-channel-hlsgroupsettings-programdatetimeperiod"></a>
The period of insertion of the EXT\-X\-PROGRAM\-DATE\-TIME entry, in seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedundantManifest`  <a name="cfn-medialive-channel-hlsgroupsettings-redundantmanifest"></a>
ENABLED: The master manifest \(\.m3u8 file\) for each pipeline includes information about both pipelines: first its own media files, then the media files of the other pipeline\. This feature allows a playout device that supports stale manifest detection to switch from one manifest to the other, when the current manifest seems to be stale\. There are still two destinations and two master manifests, but both master manifests reference the media files from both pipelines\. DISABLED: The master manifest \(\.m3u8 file\) for each pipeline includes information about its own pipeline only\. For an HLS output group with MediaPackage as the destination, the DISABLED behavior is always followed\. MediaPackage regenerates the manifests it serves to players, so a redundant manifest from MediaLive is irrelevant\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentationMode`  <a name="cfn-medialive-channel-hlsgroupsettings-segmentationmode"></a>
useInputSegmentation has been deprecated\. The configured segment size is always used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentLength`  <a name="cfn-medialive-channel-hlsgroupsettings-segmentlength"></a>
The length of the MPEG\-2 Transport Stream segments to create, in seconds\. Note that segments will end on the next keyframe after this number of seconds, so the actual segment length might be longer\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SegmentsPerSubdirectory`  <a name="cfn-medialive-channel-hlsgroupsettings-segmentspersubdirectory"></a>
The number of segments to write to a subdirectory before starting a new one\. For this setting to have an effect, directoryStructure must be subdirectoryPerStream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamInfResolution`  <a name="cfn-medialive-channel-hlsgroupsettings-streaminfresolution"></a>
The include or exclude RESOLUTION attribute for a video in the EXT\-X\-STREAM\-INF tag of a variant manifest\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Frame`  <a name="cfn-medialive-channel-hlsgroupsettings-timedmetadataid3frame"></a>
Indicates the ID3 frame that has the timecode\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimedMetadataId3Period`  <a name="cfn-medialive-channel-hlsgroupsettings-timedmetadataid3period"></a>
The timed metadata interval, in seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestampDeltaMilliseconds`  <a name="cfn-medialive-channel-hlsgroupsettings-timestampdeltamilliseconds"></a>
Provides an extra millisecond delta offset to fine tune the timestamps\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TsFileMode`  <a name="cfn-medialive-channel-hlsgroupsettings-tsfilemode"></a>
SEGMENTEDFILES: Emits the program as segments \-multiple \.ts media files\. SINGLEFILE: Applies only if the Mode field is VOD\. Emits the program as a single \.ts media file\. The media manifest includes \#EXT\-X\-BYTERANGE tags to index segments for playback\. A typical use for this value is when sending the output to AWS Elemental MediaConvert, which can accept only a single media file\. Playback while the channel is running is not guaranteed due to HTTP server caching\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)