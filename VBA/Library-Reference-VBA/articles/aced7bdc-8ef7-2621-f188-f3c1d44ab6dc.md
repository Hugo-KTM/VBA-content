
# PolicyItem Object (Office)

Represents an item within a  **ServerPolicy** object that contains the settings for one policy.


## Remarks

A policy item cannot exist outside the scope of a policy. Policy items are distinct conditions defined for a document stored on a server running Microsoft Office SharePoint Server.


## Example

The following example lists the name and description of all of the policy items for the active document.


```vb
Sub ListPolicyItems() 
Dim objSrvPolicy As ServerPolicy 
Dim objPolicyItem As PolicyItem 
Dim strPolicyItemList As String 
 
Set objSrvPolicy = ActiveDocument.ServerPolicy 
 
For Each objPolicyItem In objSrvPolicy 
 strPolicyItemList = "Policy Item " &; objPolicyItem.Name &; " - " &; _ 
 objPolicyItem.Description &; vbCrLf 
Next 
MsgBox (strPolicyItemList) 
 
End Sub
```


## See also


#### Concepts


[Object Model Reference](499c789a-aba2-0fad-649a-0ea964cd3b5e.md)
