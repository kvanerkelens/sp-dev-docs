---


manager: soliver
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
keywords:
- field type definition schema, renderpattern element (field types)
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Field Types XML
ms.assetid: d1b292bf-6be1-4372-b529-2c87d1f83d7d
---

![Collapse
section](../icons/collapse_all.gif "Collapse section")![Expand
section](../icons/expand_all.gif "Expand section")![](../icons/collapse_all.gif)![](../icons/expand_all.gif)![](../icons/dropdown.gif)![](../icons/dropdownHover.gif)![Copy
code](../icons/copycode.gif "Copy code")![Copy code
hover](../icons/copycodeHighlight.gif "Copy code hover")
<table>
<tbody>
<tr class="odd">
<td align="left"></td>
</tr>
</tbody>
</table>

Visual Basic  
C\#  
C++  
JavaScript  

<table>
<tbody>
<tr class="odd">
<td align="left"><span id="runningHeaderText"></span></td>
</tr>
<tr class="even">
<td align="left"># RenderPattern Element (Field Types)</td>
</tr>
<tr class="odd">
<td align="left"><a href="#exampleToggle">Example</a>  <a href="#seeAlsoToggle">See also</a>  <span id="headfeedbackarea" class="feedbackhead"><a href="javascript:SubmitFeedback(&#39;docthis@Microsoft.com&#39;,&#39;&#39;,&#39;&#39;,&#39;&#39;,&#39;1.0.18082.1225&#39;,&#39;%0\dThank%20you%20for%20your%20feedback.%20The%20developer%20writing%20teams%20use%20your%20feedback%20to%20improve%20documentation.%20While%20we%20are%20reviewing%20your%20feedback,%20we%20may%20send%20you%20e-mail%20to%20ask%20for%20clarification%20or%20feedback%20on%20a%20solution.%20We%20do%20not%20use%20your%20e-mail%20address%20for%20any%20other%20purpose%20and%20we%20delete%20it%20after%20we%20finish%20our%20review.%0\AFor%20further%20information%20about%20the%20privacy%20policies%20of%20Microsoft,%20please%20see%20http://privacy.microsoft.com/en-us/default.aspx.%0\A%0\d&#39;,&#39;Customer%20feedback&#39;);">Send feedback</a></span></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"></td>
</tr>
</tbody>
</table>

**Last modified:** March 09, 2015

***Applies to:** SharePoint 2016 | SharePoint Foundation 2013 |
SharePoint Online | SharePoint Server 2013*

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><img src="../icons/alert_caution.gif" title="Important note" alt="Important note" /><strong>Important</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>This topic describes markup that was used in a now obsolete method of rendering custom fields types on list views and on the Display, Edit, and New forms. It is provided solely to assist persons who are debugging a custom field type that was originally developed against an earlier version of SharePoint Foundation. For information about the recommended methods, see <a href="http://msdn.microsoft.com/library/812772eb-03d0-4a78-b212-0ba2875857df(Office.15).aspx">Field Rendering Templates</a> and <a href="http://msdn.microsoft.com/library/aacdc6d1-86c8-4a6b-953d-22ecac209d0f(Office.15).aspx">Patterns of Custom Field Rendering</a>.</p>
<p>Custom fields whose rendering is defined with **RenderPattern</span> markup still render properly on forms. However, SharePoint Foundation, by default, uses XSLT stylesheets to render fields on list views, even for legacy custom fields whose list view rendering is defined with a <span class="keyword">RenderPattern</span>. To enable the rendering of such a field, a <span class="code">&lt;Field Name=&quot;CAMLRendering&quot;&gt;TRUE&lt;/Field&gt;</span> element must be added to the containing <span class="keyword">FieldTypes</span> element in the field type definition file (<span class="code">fldtype*.xml**).</p></td>
</tr>
</tbody>
</table>

**RenderPattern** defines the actual
Collaborative Application Markup Language (CAML), HTML, and script that
SharePoint Foundation can use to render the field type in the UI. Also,
in list views, this element renders the column headers, based on the
selected field type.

<span codelanguage="other"></span>
<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><pre><code>&lt;RenderPattern Name=&quot;Text&quot;&gt;
&lt;/RenderPattern&gt;</code></pre></td>
</tr>
</tbody>
</table>


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Attribute</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>**Name**</p></td>
<td align="left"><p>Required <strong>String</strong>. Represents the name of the render pattern you are defining in this **RenderPattern** element.</p>
<p>Valid values are</p>
<ul>
<li><p>**HeaderPattern</span>. Defines rendering for the column header on list view pages when CAML rendering is turned on (by including <span class="code">&lt;Field Name=&quot;CAMLRendering&quot;&gt;TRUE&lt;/Field&gt;</span> in the containing <span class="keyword">FieldTypes</span> element of the <span class="code">fldtypes*.xml** file).</p></li>
<li><p>**DisplayPattern</span>. Defines rendering of the field for the Display (list item) form. When CAML rendering is turned on (by including <span class="code">&lt;Field Name=&quot;CAMLRendering&quot;&gt;TRUE&lt;/Field&gt;</span> in the containing <span class="keyword">FieldTypes</span> element of the <span class="code">fldtypes*.xml</span> file), then the <span class="keyword">DisplayPattern** also defines rendering of the field on list view pages.</p></li>
<li><p>**EditPattern**. Defines rendering of the field for the Edit (list item) form.</p></li>
<li><p>**NewPattern**. Defines rendering of the field for the New (list item) form.</p></li>
<li><p>**PreviewDisplayPattern**. Defines, for use in a WYSIWYG (&quot;what you see is what you get&quot;) site designer such as SharePoint Designer, a preview of how the field will look in Display mode using fictitious data.</p></li>
<li><p>**PreviewEditPattern**. Defines, for use in a WYSIWYG site designer such as SharePoint Designer, a preview of how the field will look in Edit mode using fictitious data.</p></li>
<li><p>**PreviewNewPattern**. Defines, for use in a WYSIWYG site designer such as SharePoint Designer, a preview of how the field will look in New mode using fictitious data.</p></li>
</ul></td>
</tr>
</tbody>
</table>


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>None explicitly defined, but this element is a container of CAML markup from the <span sdata="link"><a href="view-schema.htm">View Schema</a></span></p></td>
</tr>
</tbody>
</table>


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span sdata="link"><a href="fieldtype-element-field-types.htm">FieldType Element (Field Types)</a></span></p></td>
</tr>
</tbody>
</table>


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Inheritance of RenderPatterns

If a **RenderPattern** with a particular <span
class="keyword">Name</span> value is not provided for a field type, the
field type inherits the **RenderPattern** with
that name from its parent field type.

### HeaderPattern

If CAML rendering is enabled (see above), the field type must have a
**HeaderPattern** type of <span
class="keyword">RenderPattern</span> element, either directly or by
inheritance, or the column header of the field on list views does not
render. The markup in a **HeaderPattern** can
be quite simple when the field type cannot be sorted or filtered.
However, if the field type can be sorted or filtered, then the markup
can become quite complex because the header serves not just as the title
for the column but also as a drop-down menu control for sorting and
filtering. Moreover, because the ability to be sorted and filtered can
be disabled for particular columns (even when the field type the column
is based on supports them) the markup must use <span
class="keyword">Switch</span> elements to test whether sorting or
filtering is enabled for the column. See %ProgramFiles%\\Common
Files\\Microsoft Shared\\web server
extensions\\15\\TEMPLATE\\XML\\FLDTYPES.XML for examples.

### DisplayPattern

If CAML rendering is enabled (see above), a field type must have a <span
class="keyword">DisplayPattern</span> type of <span
class="keyword">RenderPattern</span> element (by inheritance, if not
directly) so that the field can be rendered on list views. This is not
necessary to render the field in Display mode, such as on the Display
(list item) page, because, a field can also be rendered in Display mode
by means of a [rendering control (.ascx
file)](http://msdn.microsoft.com/library/12616aab-f427-4abe-9e5b-8b9085a9740e(Office.15).aspx).
None of the legacy field types that ship with SharePoint Foundation use
a rendering control rather than a <span
class="keyword">DisplayPattern</span> type of <span
class="keyword">RenderPattern</span> element to render the field in
Display mode.

The **DisplayPattern** type of <span
class="keyword">RenderPattern</span> can also be used to render the
field in each row of a list view. By default, SharePoint Foundation uses
XSLT markup in a <span class="code">fldtypes\*.x</span>**s**<span
class="code">l</span> file located in %ProgramFiles%\\Common
Files\\Microsoft Shared\\web server
extensions\\15\\TEMPLATE\\LAYOUTS\\XSL to render fields on list views.
But the <span class="code">fldtypes\*.x</span>**m**<span
class="code">l</span> file in %ProgramFiles%\\Common Files\\Microsoft
Shared\\web server extensions\\15\\TEMPLATE\\XML is checked for the
presence of <span class="code">\<Field
Name="CAMLRendering"\>TRUE\</Field\></span> in the containing <span
class="keyword">FieldTypes</span> element for the field. If it is
present, the **DisplayPattern** is used to
render the field on list views.

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><img src="../icons/alert_note.gif" title="Note" alt="Note" /><strong>Note</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Two legacy field types that ship with SharePoint Foundation do not have a **DisplayPattern</span> type of <span class="keyword">RenderPattern</span> in FLDTYPES.XML: (1) <em>ContentTypeId</em> fields are never visible. (2) <em>Computed</em> fields are rendered on list views and in Display mode by a <span class="keyword">DisplayPattern</span> element in their <span class="keyword">Field** elements within the schema.xml of each list on which they appear.</p></td>
</tr>
</tbody>
</table>

### NewPattern and EditPattern

The **NewPattern** and <span
class="keyword">EditPattern</span> types of <span
class="keyword">RenderPattern</span> were used to render a field in New
mode and Edit mode, respectively, when the field did not require
significant data processing or data validation when a list item
containing the field was being created or edited. Free-form Note fields,
for example, cannot be validated because any text is a valid value.
Similarly, Choice fields and Lookup fields, by definition, limit the
user's choices to only valid values. Other fields, such as Currency and
DateTime, need only minimal validation that can be coded in script.

See %ProgramFiles%\\Common Files\\Microsoft Shared\\web server
extensions\\15\\TEMPLATE\\XML\\FLDTYPES.XML for examples of <span
class="keyword">NewPattern</span> and <span
class="keyword">EditPattern</span> types of <span
class="keyword">RenderPattern</span>s.

### RenderPatterns for MultiColumn-Derived Custom Field Types

In the **RenderPattern** markup for a custom
MultiColumn field, the **SubcolumnNumber**
attribute of a **Column** element is used to
specify an individual column in a multicolumn field type. For more
information about multicolumn field types, see [Custom Multicolumn Field
Classes](http://msdn.microsoft.com/library/62818d63-6473-42d0-b12f-251865887b33(Office.15).aspx).


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The following example defines a display rendering pattern for a custom
field type that inherits from the MultiColumn type. The field is used to
store American addresses. The first subcolumn stores the street address.
This is followed by an HTML line break. The next subcolumn stores the
city name and it is followed by a comma and a space. The third subcolumn
stores the state and, following a space, the last subcolumn stores the
postal code.

<span codelanguage="xmlLang"></span>
XML 
<span class="copyCode" onclick="CopyCode(this)"
onkeypress="CopyCode_CheckKey(this, event)"
onmouseover="ChangeCopyCodeIcon(this)"
onmouseout="ChangeCopyCodeIcon(this)" tabindex="0">![Copy
code](../icons/copycode.gif "Copy code")Copy code</span>
    <RenderPattern Name="DisplayPattern">
      <Switch>
        <Expr><Column/></Expr>
        <Case Value="">
        </Case>
        <Default>
          <Column SubColumnNumber="0" HTMLEncode="TRUE"/>
          <HTML><![CDATA[<BR>]]></HTML>
          <Column SubColumnNumber="1" HTMLEncode="TRUE"/>
          <HTML><![CDATA[, &nbsp;]]></HTML>
          <Column SubColumnNumber="2" HTMLEncode="TRUE"/>
          <HTML><![CDATA[ &nbsp;]]></HTML>
          <Column SubColumnNumber="3" HTMLEncode="TRUE"/>
          </Default>
      </Switch>
    </RenderPattern>


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Other resources

[Walkthrough: Creating a Custom Field
Type](http://msdn.microsoft.com/library/089a1b8a-cafc-4050-b445-16650602fe4f(Office.15).aspx)

[Custom Field
Types](http://msdn.microsoft.com/library/1345b345-226d-443a-918f-af123a3c7b13(Office.15).aspx)

[Custom Field
Classes](http://msdn.microsoft.com/library/436a9d9b-7a6f-4e8f-86e8-f42ded85c069(Office.15).aspx)

[Custom Field Type Property
Rendering](http://msdn.microsoft.com/library/a959ad5b-6f3a-462c-80b9-e2d00bb0d62a(Office.15).aspx)

[Custom Field Type
Definition](http://msdn.microsoft.com/library/b3315997-671f-4c29-9518-48cc4592f205(Office.15).aspx)

[Custom Multicolumn Field
Classes](http://msdn.microsoft.com/library/62818d63-6473-42d0-b12f-251865887b33(Office.15).aspx)







