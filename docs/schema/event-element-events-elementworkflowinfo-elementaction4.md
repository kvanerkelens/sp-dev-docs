---
ms.author: kenwith
author: kenwith
manager: laurawi
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af057e04-856c-3f9d-e62b-e08242956d7a
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
<td align="left"># Event element (Events element) (WorkflowInfo element) (Action4)</td>
</tr>
<tr class="odd">
<td align="left"><span id="headfeedbackarea" class="feedbackhead"><a href="javascript:SubmitFeedback(&#39;docthis@Microsoft.com&#39;,&#39;&#39;,&#39;&#39;,&#39;&#39;,&#39;1.0.18082.1225&#39;,&#39;%0\dThank%20you%20for%20your%20feedback.%20The%20developer%20writing%20teams%20use%20your%20feedback%20to%20improve%20documentation.%20While%20we%20are%20reviewing%20your%20feedback,%20we%20may%20send%20you%20e-mail%20to%20ask%20for%20clarification%20or%20feedback%20on%20a%20solution.%20We%20do%20not%20use%20your%20e-mail%20address%20for%20any%20other%20purpose%20and%20we%20delete%20it%20after%20we%20finish%20our%20review.%0\AFor%20further%20information%20about%20the%20privacy%20policies%20of%20Microsoft,%20please%20see%20http://privacy.microsoft.com/en-us/default.aspx.%0\A%0\d&#39;,&#39;Customer%20feedback&#39;);">Send feedback</a></span></td>
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

Specifies a workflow event from among available workflow events. 

**Last modified:** March 09, 2015

***Applies to:** SharePoint Server 2013*


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<span codelanguage="xmlLang"></span>
XML 
<span class="copyCode" onclick="CopyCode(this)"
onkeypress="CopyCode_CheckKey(this, event)"
onmouseover="ChangeCopyCodeIcon(this)"
onmouseout="ChangeCopyCodeIcon(this)" tabindex="0">![Copy
code](../icons/copycode.gif "Copy code")Copy code</span>
    <events>
        <event />
    </events


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span class="label">Element type</span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span class="label">Namespace</span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span class="label">Schema file</span></p></td>
<td align="left"><p>Actions4.xsd</p></td>
</tr>
</tbody>
</table>


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<span codelanguage="xmlLang"></span>
XML 
<span class="copyCode" onclick="CopyCode(this)"
onkeypress="CopyCode_CheckKey(this, event)"
onmouseover="ChangeCopyCodeIcon(this)"
onmouseout="ChangeCopyCodeIcon(this)" tabindex="0">![Copy
code](../icons/copycode.gif "Copy code")Copy code</span>
    <xs:element name="Event" minOccurs="0" maxOccurs="unbounded">
         <xs:attribute name="Name" type="s:string" use="required" />
         <xs:attribute name="DisplayName" type="s:string" use="required" />
         <xs:attribute name="EventGroup" type="s:string" use="required" />
         <xs:attribute name="Category" type="s:string" use="required" />
         <xs:attribute name="RankDefault" type="s:string" use="required" />
      </xs:element>  


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

If the schema defines specific requirements, such as <span
class="keyword">sequence</span>, **minOccurs**,
**maxOccurs**, and <span
class="keyword">choice</span>, see the definition section.

### Parent elements

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Element</p></th>
<th align="left"><p>Type</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="events-element-workflowinfo-elementaction4.htm">Events</a></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

### Child elements

None.

### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Attribute</p></th>
<th align="left"><p>Type</p></th>
<th align="left"><p>Required</p></th>
<th align="left"><p>Description</p></th>
<th align="left"><p>Possible values</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Category</p></td>
<td align="left"><p>s:string</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p>The category associated with the event; for example, **ListItemEvent</span> or <span class="keyword">ProjectEvent**.</p></td>
<td align="left"><p>Values of the s:string type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>s:string</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p>The name of the event as rendered in the user interface.</p></td>
<td align="left"><p>Values of the s:string type.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EventGroup</p></td>
<td align="left"><p>s:string</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p>The display name of the event group as rendered in the user interface; for example, <span class="ui">Project Web App Event</span>.</p></td>
<td align="left"><p>Values of the s:string type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>s:string</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p>The programmatic name of the event; for example, **ItemAdded</span>, <span class="keyword">ItemUpdated**. This value originates in the list of events supported by SharePoint Foundation and Project Server 2013.</p></td>
<td align="left"><p>Values of the s:string type.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RankDefault</p></td>
<td align="left"><p>s:string</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p>Specifies the sort order of the event when rendered in the user interface.</p></td>
<td align="left"><p>Values of the s:string type.</p></td>
</tr>
</tbody>
</table>

![Footer](../icons/footer.gif "Footer")

[© 2013 Microsoft Corporation. All rights
reserved.](office-2013-documentation-copyright-notice.htm)


