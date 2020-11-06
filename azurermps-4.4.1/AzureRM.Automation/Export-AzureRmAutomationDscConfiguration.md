---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: ed35cf910dd0bf51803b6a38edc90a93f5411520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587002"
---
# Export-AzureRmAutomationDscConfiguration

## SYNOPSIS
Bir DSC yapılandırmasını otomasyondan yerel dosyaya aktarır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Export-AzureRmAutomationDscConfiguration** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) yapılandırmasını Azure Otomasyonu 'ndan yerel dosyaya aktarır.
Dışarı aktarılan dosyanın. ps1 dosya adı uzantısı vardır.

## ÖRNEKLERDEN

### Örnek 1: DSC yapılandırmasının yayımlanmış sürümünü dışarı aktarma
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

Bu komut, bir DSC yapılandırmasının yayımlanan sürümünü Otomasyon 'daki belirtilen klasöre (Masaüstü) dışarı aktarır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in dışarı aktardığı DSC 'yi içeren Otomasyon hesabının adını belirtir.

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

### -Force
Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in dışarı aktardığı DSC yapılandırmasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputFolder
Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı çıkış klasörünü belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı kaynak grubunun adını belirtir.

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

### Yuvalı
Bu cmdlet 'in DSC yapılandırmasının hangi sürümünü dışarı aktaracağını belirtir.
Geçerli değerler: 

- Lar
- Yayımlanabilir 

Varsayılan değer yayımlanır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### System. ıO. DirectoryInfo

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)

[Import-AzureRmAutomationDscConfiguration](./Import-AzureRmAutomationDscConfiguration.md)


