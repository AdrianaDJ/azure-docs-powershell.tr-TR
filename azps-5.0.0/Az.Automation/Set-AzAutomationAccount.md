---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323437"
---
# Set-AzAutomationAccount

## SYNOPSIS
Otomasyon hesabını değiştirir.

## INDEKI

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzAutomationAccount** cmdlet 'ı bir Azure Otomasyonu hesabını değiştirir.
Otomasyon hesapları hakkında daha fazla bilgi için New-AzAutomationAccount cmdlet bölümüne bakın.

## ÖRNEKLERDEN

### Örnek 1: Otomasyon hesabının etiketlerini ayarlama
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

İlk komut $Tags değişkenine iki anahtar/değer çifti atar.
İkinci komut, AutomationAccount01 adlı Otomasyon hesabı için $Tags etiketleri ayarlar.

### Örnek 2: Otomasyon hesabı için planı değiştirme
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

Bu komut, AutomationAccount01 adlı Otomasyon hesabı için planı temel olarak değiştirir.

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
Bu cmdlet 'in değiştirdiği Otomasyon hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Otomasyon hesabı için planı belirtir.
Geçerli değerler:
- Ana
- Bırakılamıyor

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in değiştirdiği Otomasyon hesabını içeren bir kaynak grubunun adını belirtir.

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

### -Etiketler
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. topluluklar. IDictionary

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. AutomationAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationAccount](./Get-AzAutomationAccount.md)

[Yeni-AzAutomationAccount](./New-AzAutomationAccount.md)

[Remove-AzAutomationAccount](./Remove-AzAutomationAccount.md)
