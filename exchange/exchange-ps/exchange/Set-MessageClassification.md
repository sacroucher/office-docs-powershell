---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Set-MessageClassification

## SYNOPSIS
!!! Exchange Server 2010

Use the Set-MessageClassification cmdlet to configure an existing message classification instance in your Exchange organization.

!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Set-MessageClassification cmdlet to configure an existing message classification instance in your organization.

## SYNTAX

```
Set-MessageClassification [-Identity] <MessageClassificationIdParameter> [-ClassificationID <Guid>] [-Confirm]
 [-DisplayName <String>]
 [-DisplayPrecedence <Highest | Higher | High | MediumHigh | Medium | MediumLow | Low | Lower | Lowest>]
 [-DomainController <Fqdn>] [-Name <String>] [-PermissionMenuVisible <$true | $false>]
 [-RecipientDescription <String>] [-RetainClassificationEnabled <$true | $false>] [-SenderDescription <String>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Message classifications" entry in the Transport Permissions topic.

!!! Exchange Server 2013

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Message classifications" entry in the Mail flow permissions topic.

!!! Exchange Server 2016, Exchange Online

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Set-MessageClassification -Identity MyMessageClassification -DisplayPrecedence Low -RetainClassificationEnabled $false
```

This example makes the following configuration changes to the message classification MyMessageClassification:


Changes the display precedence to Low.

Specifies that the message classification shouldn't persist with the message if the message is forwarded or replied to.

### Example 1 -------------------------- (Exchange Server 2013)
```
Set-MessageClassification MyMessageClassification -DisplayPrecedence Low -RetainClassificationEnabled $false
```

This example makes the following configuration changes to the message classification named MyMessageClassification:


Changes the display precedence to Low.

Specifies that the message classification shouldn't persist with the message if the message is forwarded or replied to.

### Example 1 -------------------------- (Exchange Server 2016)
```
Set-MessageClassification MyMessageClassification -DisplayPrecedence Low -RetainClassificationEnabled $false
```

This example makes the following configuration changes to the message classification named MyMessageClassification:


Changes the display precedence to Low.

Specifies that the message classification shouldn't persist with the message if the message is forwarded or replied to.

### Example 1 -------------------------- (Exchange Online)
```
Set-MessageClassification MyMessageClassification -DisplayPrecedence Low -RetainClassificationEnabled $false
```

This example makes the following configuration changes to the message classification named MyMessageClassification:


Changes the display precedence to Low.

Specifies that the message classification shouldn't persist with the message if the message is forwarded or replied to.

## PARAMETERS

### -Identity
!!! Exchange Server 2010

The Identity parameter specifies the name or GUID of the message classification. This parameter can take a string value.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The Identity parameter specifies the name or GUID of the message classification you want to modify.



```yaml
Type: MessageClassificationIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ClassificationID
!!! Exchange Server 2010

The ClassificationID parameter specifies a GUID of an existing message classification that you want to use in your Exchange organization. Use this parameter if you're configuring message classifications to span two Exchange forests in the same organization.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The ClassificationID parameter specifies the GUID of an existing message classification that you want to use in your Exchange organization. Use this parameter if you're configuring message classifications to span two Exchange forests in the same organization.



```yaml
Type: Guid
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
!!! Exchange Server 2010

The DisplayName parameter specifies the display name for the message classification instance. The display name appears in the 2007 Microsoft Office system and is used by Microsoft Outlook users to select the appropriate message classification before they send a message.

When you specify a name that includes spaces, you must enclose the name in quotation marks ("), for example, "Display Name". The DisplayName parameter must contain a maximum of 64 characters.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The DisplayName parameter specifies the display name for the message classification instance. The display name appears in the Microsoft Office and is used by Outlook users to select the appropriate message classification before they send a message.

When you specify a name that includes spaces, you must enclose the name in quotation marks ("), for example, "Display Name". The DisplayName parameter can contain a maximum of 64 characters.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayPrecedence
!!! Exchange Server 2010

The DisplayPrecedence parameter specifies the relative precedence of the message classification to other message classifications that may be applied to a specified message. Although Outlook only lets a user specify a single classification on a specified message, transport rules may apply other classifications. This parameter sets the precedence on a specified classification for what's displayed to the recipient in Outlook. The classification with the highest precedence is shown first, and the subsequent classifications, which are those with lesser precedence as defined by this parameter, are appended in the appropriate order thereafter.

Valid input for the DisplayPrecedence parameter is Highest, Higher, High, MediumHigh, Medium, MediumLow, Low, Lower, and Lowest.

The default value is Medium.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The DisplayPrecedence parameter specifies the relative precedence of the message classification to other message classifications that may be applied to a specified message. Although Outlook only lets a user specify a single classification for each message, transport rules may apply other classifications to a message. The classification with the highest precedence is shown first, and the subsequent classifications, which are those with lesser precedence as defined by this parameter, are appended in the appropriate order thereafter.

Valid input for the DisplayPrecedence parameter is Highest, Higher, High, MediumHigh, Medium, MediumLow, Low, Lower, and Lowest.

The default value is Medium.



```yaml
Type: Highest | Higher | High | MediumHigh | Medium | MediumLow | Low | Lower | Lowest
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
!!! Exchange Server 2010

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

The DomainController parameter isn't supported on Edge Transport servers. An Edge Transport server uses the local instance of Active Directory Lightweight Directory Services (AD LDS) to read and write data.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

The DomainController parameter isn't supported on Edge Transport servers. An Edge Transport server uses the local instance of Active Directory Lightweight Directory Services (AD LDS) to read and write data.



```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
!!! Exchange Server 2010

The Name parameter specifies the administrative name for the message classification instance. The name is used to administer the message classification instance. When you specify a name that includes spaces, you must enclose the name in quotation marks ("), for example, "Adminstrative Name". The Name parameter must contain a maximum of 256 characters.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The Name parameter specifies the administrative name for the message classification instance. The name is used to administer the message classification instance. When you specify a name that includes spaces, you must enclose the name in quotation marks ("), for example, "Administrative Name". The Name parameter can contain a maximum of 256 characters.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionMenuVisible
!!! Exchange Server 2010

The PermissionMenuVisible parameter specifies whether the values that you entered for the DisplayName and RecipientDescription parameters are displayed in the recipient's Outlook message as they're composing a message.

If you set the PermissionMenuVisible parameter to $false, users won't be able to assign this message classification to the messages they're composing. However, messages received with this message classification still display the classification information.

The default value is $true.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The PermissionMenuVisible parameter specifies whether the values that you entered for the DisplayName and RecipientDescription parameters are displayed in Outlook as the user composes a message.

If you set the PermissionMenuVisible parameter to $false, users won't be able to assign this message classification to the messages they're composing. However, messages received with this message classification still display the classification information.

The default value is $true.



```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecipientDescription
!!! Exchange Server 2010

The RecipientDescription parameter specifies to the recipient what the message classification is intended to achieve. The text you enter in this parameter is viewed by Outlook users when they receive a message that has this message classification. Enclose the description in quotation marks ("), for example, "This is the recipient description that explains how to treat the message that has been classified". The RecipientDescription parameter can contain a maximum of 1,024 characters.

If you don't enter a value for this parameter, the description that you enter for SenderDescription is used.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The RecipientDescription parameter specifies the purpose of the message classification to the recipient. The value of this parameter is shown to Outlook users when they receive a message that has this message classification. Enclose the value in quotation marks ("), for example, "This is the recipient description that explains how to treat the message that has been classified". The RecipientDescription parameter can contain a maximum of 1,024 characters.

If you don't enter a value for this parameter, the description that you enter for SenderDescription is used.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetainClassificationEnabled
The RetainClassificationEnabled parameter specifies whether the message classification should persist with the message if the message is forwarded or replied to.

The default value is $true.

```yaml
Type: $true | $false
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SenderDescription
!!! Exchange Server 2010

The SenderDescription parameter specifies to the sender what the message classification is intended to achieve. The text you enter in this parameter is used by Outlook users to select the appropriate message classification before they send a message. Enclose the description in quotation marks ("), for example, "This is the sender description that explains when to use this message classification". The SenderDescription parameter can contain a maximum of 1,024 characters.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

The SenderDescription parameter specifies the purpose of the message classification to the sender. The value of this parameter is used by Outlook users to select the appropriate message classification before they send a message. Enclose the value in quotation marks ("), for example, "This is the sender description that explains when to use this message classification". The SenderDescription parameter can contain a maximum of 1,024 characters.



```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/fdbe9e1d-6e92-4ab7-9a77-88814c0eda68.aspx)

