---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6f53573c6eb737d280ac24182ed84158d63d132f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321833"
---
# Register-AzAutomationScheduledRunbook

## SYNOPSIS
Bir runbook 'u zamanlamaya ilişkilendirir.

## INDEKI

### ByRunbookName (varsayılan)
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Register-AzAutomationScheduledRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu bir zamanlamayla ilişkilendirir.
Runbook, *ScheduleName* parametresini kullanarak belirttiğiniz zamanlamaya göre başlar.

## ÖRNEKLERDEN

### Örnek 1: bir runbook 'u zamanlamayla Ilişkilendirme
```powershell
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

Bu komut, Runbk01 adlı runbook 'u Contoso17 adlı Azure Otomasyon hesabındaki Sched01 adlı zamanlamayla ilişkilendirir.

### Örnek 2

Bir runbook 'u zamanlamaya ilişkilendirir. oluşturulmuş

<!-- Aladdin Generated Example -->
```powershell
Register-AzAutomationScheduledRunbook -AutomationAccountName 'Contoso17' -Parameters <IDictionary> -ResourceGroupName 'ResourceGroup01' -RunbookName 'Runbk01' -ScheduleName 'Sched01'
```

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametreler
Anahtar/değer çiftleri karma tablosunu belirtir.
Anahtarlar, runbook parametre adlarıdır.
Değerler runbook parametre değerleridir.
Runbook ilişkili zamanlama tamamlandığında başlatıldığında, bu parametreler runbook 'a geçirilir.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Zamanlanmış runbook için kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunbookName
Bu cmdlet 'in zamanlamada ilişki kurduğu runbook 'un adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Karma Runbook Worker grubunun adı.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Bu cmdlet 'in runbook 'u ilişkilendiren zamanlamanın adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Jobzamanlama

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationScheduledRunbook](./Get-AzAutomationScheduledRunbook.md)

[Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md)


