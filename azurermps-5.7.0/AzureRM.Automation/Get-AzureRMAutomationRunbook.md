---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: d9ffd6ae2f7695a02f8c29fbe745202642039af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594503"
---
# Get-AzureRmAutomationRunbook

## SYNOPSIS
Runbook alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tümü (varsayılan)
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationRunbook** cmdlet 'ı Azure Otomasyonu runbook 'unu alır.
Belirli bir runbook almak için adını belirtin.

## ÖRNEKLERDEN

### Örnek 1: tüm runbook 'ları alma
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm runbook 'ları alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in runbook 'ları aldığı Otomasyon hesabının adını belirtir.

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

### -Ad
Bu cmdlet 'in aldığı runbook 'un adını belirtir.

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in runbook 'ları aldığı kaynak grubun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. runbook

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Dışarı aktarma-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[Import-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[Yeni-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Yeni-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Yayımlama-AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[Remove-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)

[Start-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)


