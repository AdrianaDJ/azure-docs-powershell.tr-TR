---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ec89359453af2dd997aed6359914ac499a6a3f7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587709"
---
# Register-AzureRmAutomationScheduledRunbook

## SYNOPSIS
Bir runbook 'u zamanlamaya ilişkilendirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByRunbookName (varsayılan)
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Register-AzureRmAutomationScheduledRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu bir zamanlamayla ilişkilendirir.
Runbook, *ScheduleName* parametresini kullanarak belirttiğiniz zamanlamaya göre başlar.

## ÖRNEKLERDEN

### Örnek 1: bir runbook 'u zamanlamayla Ilişkilendirme
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

Bu komut, Runbk01 adlı runbook 'u Contoso17 adlı Azure Otomasyon hesabındaki Sched01 adlı zamanlamayla ilişkilendirir.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: IDictionary
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
Type: String
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Jobzamanlama

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAutomationScheduledRunbook](./Get-AzureRMAutomationScheduledRunbook.md)

[Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRMAutomationScheduledRunbook.md)


