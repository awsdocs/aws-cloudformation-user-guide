# Integrated JSON and YAML editor<a name="working-with-templates-cfn-designer-json-editor"></a>

Use Designer's integrated JSON and YAML editor to view and edit template details\. For example, you can use the integrated editor to define the properties of a resource or to change a template parameter\. The integrated editor has two views: a **Components** view and a **Template** view\.

To make minor changes to a specific section of a template, use the **Components** view\. In the **Components** view, the components that you can edit are divided into tabs\. These tabs change depending on whether you have a resource selected\.

For example, if you select a resource, Designer provides tabs to edit the resource's properties and attributes, such as an update policy or creation policy\. If you haven't selected anything, Designer provides tabs for editing the template parameters, mappings, conditions, metadata, and outputs\. Any changes that you make in the **Components** view must be valid JSON or YAML markup\. If you introduce invalid JSON or YAML, Designer reverts the invalid markup to the valid markup when you leave the **Components** view\.

To make broad changes to your template, use the **Template** view\. In the **Template** view, the integrated JSON and YAML editor shows you the raw JSON or YAML of your entire template\. When you want to make changes to a resource, select it in the canvas pane\. Designer automatically highlights that resource in the integrated JSON and YAML editor\.

**AWS CloudFormation Designer integrated JSON and YAML editor**

![\[Screenshot of the integrated JSON and YAML editor with raw JSON.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-jsoneditor.png)

## Converting templates into YAML or JSON<a name="w7739ab1c27c17c13c17c15"></a>

You can convert a valid template back and forth between JSON and YAML by selecting the appropriate radio button in **Choose template language**\. Designer can only convert valid YAML or valid JSON templates\. If the conversion succeeds, the **Messages** pane displays a message like: *Successfully converted the template to YAML*\. 

**Important**  
We recommend that you do not add `#` YAML comments to your templates in Designer\. If your YAML template has `#` comments, Designer doesn't preserve those comments when editing the YAML or converting to JSON\. If you edit or modify your template in Designer \(for example, if you drag a resource on the canvas\), your comments are lost\.

Once you choose a template language, any new resources you drag onto the canvas will be created in the language you have selected\. To change back to another language, make sure your template is valid and then select **YAML** or **JSON** where it says **Choose template language**\.

**Note**  
When you convert a template to YAML, Designer uses short form notation for functions\. For example, `- !GetAtt`\. In addition, any visual links that you draw will use short form notation in YAML mode\. For more information about intrinsic functions, see [`Ref`](intrinsic-function-reference-ref.md)\.

## Autocomplete<a name="w7739ab1c27c17c13c17c17"></a>

The integrated JSON and YAML editor includes an auto\-complete feature that helps you specify resource properties, so you don't have to remember property names\. To see a list of valid properties in a JSON template, press **Ctrl\+Space** within the `Properties` curly braces \(`{}`\), as shown in the following example:

![\[Autocomplete options in a JSON example.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-jsoneditor-autocomplete.png)

For a YAML template, you can first delete the opening and closing curly braces and press **Enter** to go to a new line\. To see a list of valid properties, press **Ctrl\+Space** on the new line after `Properties`, as shown in the following example:

![\[Autocomplete options in a YAML example.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-yamleditor-autocomplete.png)

## Keyboard shortcuts<a name="w7739ab1c27c17c13c17c19"></a>

Designer's integrated JSON and YAML editor provides the following keyboard shortcuts:

Ctrl\+Space  
Within the `Properties` key of a resource, lists all of the available properties for the resource\.

Ctrl\+F  
Searches for a specified value\.  
To highlight everything that matches the specified value, press **Alt\+Enter**\.