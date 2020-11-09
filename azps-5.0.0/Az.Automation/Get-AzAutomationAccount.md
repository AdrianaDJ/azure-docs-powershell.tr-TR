---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322657"
---
# Get-AzAutomationAccount

## SYNOPSIS
Kaynak grubundaki Otomasyon hesaplarını alır.

## INDEKI

### Tümü (varsayılan)
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAutomationAccountName
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzAutomationAccount** cmdlet 'i, kaynak grubundaki Azure Otomasyonu hesaplarını alır.
Otomasyon hesapları hakkında daha fazla bilgi için New-AzAutomationAccount cmdlet bölümüne bakın.

## ÖRNEKLERDEN

### Örnek 1: tüm hesapları alma
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

Bu komut, ResourceGroup03 adlı kaynak grubundaki tüm otomasyon hesaplarını alır.

### Örnek 2: hesap alma
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoAutomationAccount adlı Otomasyon hesabını alır.

## PARAMETRELERINE

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

### -Ad
Bu cmdlet 'in aldığı Otomasyon hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in Otomasyon hesaplarını aldığı kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. AutomationAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzAutomationAccount](./New-AzAutomationAccount.md)

[Remove-AzAutomationAccount](./Remove-AzAutomationAccount.md)

[Set-AzAutomationAccount](./Set-AzAutomationAccount.md)


