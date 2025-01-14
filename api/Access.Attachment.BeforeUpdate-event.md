---
title: Attachment.BeforeUpdate event (Access)
keywords: vbaac10.chm14019
f1_keywords:
- vbaac10.chm14019
ms.prod: access
api_name:
- Access.Attachment.BeforeUpdate
ms.assetid: 0437e831-b96f-60b6-1a7c-3e1f720394b7
ms.date: 02/07/2019
ms.localizationpriority: medium
---


# Attachment.BeforeUpdate event (Access)

The **BeforeUpdate** event occurs before changed data in a control or record is updated.


## Syntax

_expression_.**BeforeUpdate** (_Cancel_)

_expression_ A variable that represents an **[Attachment](Access.Attachment.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Cancel_|Required|**Integer**|The setting determines if the **BeforeUpdate** event occurs. Setting the _Cancel_ argument to **True** (1) cancels the **BeforeUpdate** event.|

## Return value

Nothing


## Remarks

Changing data in a control by using Visual Basic or a macro containing the SetValue action doesn't trigger these events for the control. However, if you then move to another record or save the record, the form's **BeforeUpdate** event does occur.

The **BeforeUpdate** event applies only to controls on a form, not controls on a report.

To run a macro or event procedure when this event occurs, set the **[BeforeUpdate](access.attachment.beforeupdate-property.md)** property to the name of the macro or to [Event Procedure].

The **BeforeUpdate** event is triggered when a control or record is updated. Within a record, changed data in each control is updated when the control loses the focus or when the user presses Enter or Tab. When the focus leaves the record or if the user chooses **Save Record** on the **Records** menu, the entire record is updated, and the data is saved in the database.

When you enter new or changed data in a control on a form and then move to another record, or save the record by choosing **Save Record** on the **Records** menu, the **AfterUpdate** event for the form occurs immediately after the **AfterUpdate** event for the control. When you move to a different record, the **Exit** and **LostFocus** events for the control occur, followed by the **Current** event for the record you moved to, and the **Enter** and **GotFocus** events for the first control in this record. To run the **AfterUpdate** macro or event procedure without running the **Exit** and **LostFocus** macros or event procedures, save the record by using the **Save Record** command on the **Records** menu.

**BeforeUpdate** macros and event procedures run only if you change the data in a control. This event does not occur when a value changes in a calculated control. **BeforeUpdate** macros and event procedures for a form run only if you change the data in one or more controls in the record.

If the user enters a new value in the control, the **OldValue** property setting isn't changed until the data is saved (the record is updated). If you cancel an update, the value of the **OldValue** property replaces the existing value in the control.

You often use the **BeforeUpdate** event to validate data, especially when you perform complex validations, such as those that:

- Involve conditions for more than one value on a form.   
- Display different error messages for different data entered.   
- Can be overridden by the user.   
- Contain references to controls on other forms or contain user-defined functions. 
    
A run-time error occurs if you attempt to modify the data contained in the control that fired the **BeforeUpdate** event in the event's procedure.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]