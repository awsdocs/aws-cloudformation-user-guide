# Release history for AWS CloudFormation helper scripts<a name="releasehistory-aws-cfn-bootstrap"></a>

The following table describes the changes to the aws\-cfn\-bootstrap package, which contains the AWS CloudFormation helper scripts\. 

You can also download the latest version of the helper scripts at the following links\. These links redirect to the most recent version of the helper scripts listed in the table below\. 
+ [ TAR\.GZ](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-latest.tar.gz)
+ [ ZIP](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-latest.zip)
+ [ EXE \(32\-bit Windows\)](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-latest.exe)
+ [ EXE \(64\-bit Windows\)](https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-win64-latest.exe)

**Note**  
Version 2\.0\-1 and above of the helper scripts support Python 3\.4 and above\. If you need helper scripts that support an earlier version of Python, see [Release History for CloudFormation Helper Scripts 1\.4](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html#releasehistory-aws-cfn-bootstrap-v1)\.


| Version | Release Date | Change Description | Download Packages | 
| --- | --- | --- | --- | 
|  2\.0\-2 \(Latest; recommended\)  |  9/14/2020  |  The default and user specified interval for `cfn-hup` has an accuracy of plus or minus 30 seconds\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  2\.0\-1  |  6/24/2020  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 

## Release History for CloudFormation Helper Scripts 1\.4<a name="releasehistory-aws-cfn-bootstrap-v1"></a>

The table below provides access to previous versions of the helper scripts, which support Python version 2\.7 and 2\.6\. It is provided for backwards compatibility\. We recommend using the latest version of the helper scripts, which require Python 3\.4 or above\.

**Note**  
The AWS CloudFormation helper scripts are preinstalled on Amazon Linux AMI images\. The download packages listed in the table apply to other Linux/Unix distributions and Microsoft Windows \(2008 or later\)\. To learn how to use the helper scripts, see [CloudFormation helper scripts reference](cfn-helper-scripts-reference.md)\.


| Version | Release date | Change description | Download packages | 
| --- | --- | --- | --- | 
|  1\.4\-34  |  9/14/2020  |  The default and user specified interval for `cfn-hup` has an accuracy of plus or minus 30 seconds\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-33  |  5/28/2020  |  Supports Python 2\.6 and 2\.7\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-32   |    |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |   | 
|  1\.4\-31  |  9/10/2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-30  |  3/21/2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-29   |  2/12/2018  |  Extending support for newer AWS regions\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-27  |  1/24/2018  |  Extending support for newer AWS regions\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-24,1\.4\-26  |  10/12/2017  |  Fixed an incompatibility for customers using an older version of Python\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-23  |  10/3/2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-22  |  9/14/2017  |  Changed `umask` default value from `0` to `0022`\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-21  |  8/31/2017  |  Added the `umask` parameter for the cfn\-hup daemon, with a default value of `0`\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-20  |  8/2/2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 
|  1\.4\-19  |  7/20/2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/releasehistory-aws-cfn-bootstrap.html)  | 