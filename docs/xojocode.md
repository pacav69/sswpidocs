

version As String

A short text description for the app. Usually this contains just the version number (such as 1.2.3.4) and is displayed by some operating systems in Get Info or Property windows for the app. This property can be set only in the IDE.

This property is read-only.

Typically version numbers are written as 1.2.3.4.

Version is displayed by the file information windows on macOS (Finder, Get Info) and Windows (Windows Explorer, Properties).

Display the short version:

MessageBox(App.Version)

=============== display github markdown page

Dim T As String
T = "https://github.com/pacav69/sswpidev/blob/main/docs/shortcutkeys.md"
ShowURL T
Return True


============== dialog box

Var d As New MessageDialog                  ' declare the MessageDialog object
Var b As MessageDialogButton                ' for handling the result
d.IconType = MessageDialog.IconTypes.Caution ' display warning icon
d.ActionButton.Caption = "Save"
d.CancelButton.Visible = True               ' show the Cancel button
d.AlternateActionButton.Visible = True      ' show the "Don't Save" button
d.AlternateActionButton.Caption = "Don't Save"
d.Message = "Do you want to save changes to this document before closing?"
d.Explanation = "If you don't save, your changes will be lost. "

b = d.ShowModal                             ' display the dialog
Select Case b                               ' determine which button was pressed.
Case d.ActionButton
  ' user pressed Save
Case d.AlternateActionButton
  ' user pressed Don't Save
Case d.CancelButton
  ' user pressed Cancel
End Select
Return True



=================== MessageDialog

'Dim d As MessageDialog d = New MessageDialog

''b=d.ShowModalWithin(self)                              //display the dialog
'
'Variant d as new MessageDialog
'
'
'Var d As New MessageDialog                  ' declare the MessageDialog object
'Var b As MessageDialogButton                ' for handling the result
'd.IconType = MessageDialog.IconTypes.Caution ' display warning icon
'd.ActionButton.Caption = "Save"
'd.CancelButton.Visible = True               ' show the Cancel button
'd.AlternateActionButton.Visible = True      ' show the "Don't Save" button
'd.AlternateActionButton.Caption = "Don't Save"
'd.Message = "Do you want to save changes to this document before closing?"
'd.Explanation = "If you don't save, your changes will be lost. "
'
'b = d.ShowModal                             ' display the dialog
'Select Case b                               ' determine which button was pressed.
'Case d.ActionButton
'' user pressed Save
'Case d.AlternateActionButton
'' user pressed Don't Save
'Case d.CancelButton
'' user pressed Cancel
'End Select
'Return True


========================= MessageDialog

Var dialog As New MessageDialog
dialog.Message = "Do you want to save changes to this document before closing?"
dialog.ActionButton.Caption = "Save"
dialog.CancelButton.Visible = True
dialog.CancelButton.Caption = "Cancel"
dialog.AlternateActionButton.Visible = True
dialog.AlternateActionButton.Caption = "Don't Save"
Var dialogButton As MessageDialogButton
dialogButton = dialog.ShowModalWithin(Self)
Select Case dialogButton
  Case dialog.ActionButton
    ' Save
  Case dialog.AlternateActionButton
    ' Don't save
  Case dialog.CancelButton
    ' Cancel
End Select


======================

MessageBox("File transfer complete!")

==================================
key shortcut

#App.kFileQuitShortcut
