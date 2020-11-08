---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106357"
---
# Get-AzureAutomationScheduledRunbook

## SYNOPSIS

Azure Otomasyonu runbook 'ları ve ilişkili zamanlamaları alır.

## INDEKI

### Tümü (varsayılan)
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Byjobscheduleıd
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationScheduledRunbook** , bir veya daha fazla Azure Automation runbook 'u ve ilişkili zamanlamaları alır.
Varsayılan olarak, tüm zamanlanmış runbook 'lar döndürülür.

Belirli bir planlı runbook almak için Runbook adını ve zamanlama adını belirtin.
Runbook ile ilişkili tüm zamanlamaları almak için yalnızca runbook adını belirtin.
Bir zamanlamayla ilişkilendirilmiş tüm runbook 'ları almak için yalnızca zamanlama adını belirtin.

## ÖRNEKLERDEN

### Örnek 1: tüm zamanlanmış runbook 'ları alma
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm zamanlanmış runbook 'ları alır.

### Örnek 2: runbook ile ilişkili tüm zamanlamaları alma
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

Bu komut, Contoso17 adındaki Otomasyon hesabındaki runbook Runbk01 için tüm zamanlanmış runbook 'ları alır.

### Örnek 3: zamanlamayla ilişkili tüm runbook 'ları alma
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

Bu komut, Contoso17 adındaki Otomasyon hesabındaki zamanlama Schedule01 için tüm zamanlanmış runbook 'ları alır.

## PARAMETRELERINE

### -AutomationAccountName
Azure Otomasyonu hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jobscheduleıd
Zamanlanmış işin KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunbookName
Runbook 'un adını belirtir.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Bir zamanlamanın adını belirtir.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Jobzamanlama

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Register-AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Unregister-AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


