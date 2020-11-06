---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 5a222b404aa931cec468ee5dfc66963f48b23ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587221"
---
# Remove-AzureRmOperationalInsightsWorkspace

## SYNOPSIS
Çalışma alanını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanını siler.
Bu çalışma alanı, oluşturma sırasında *MüşteriNo* parametresi aracılığıyla varolan bir hesaba bağlanmışsa, çalışma

## ÖRNEKLERDEN

### Örnek 1: çalışma alanını adla kaldırma
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

Bu komut MyWorkspace adlı çalışma alanını ContosoResourceGroup adlı kaynak grubundan kaldırır.

### Örnek 2: ardışık düzeni kullanarak bir çalışma alanını kaldırma
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından bunu kaldırmak için ardışık düzen işlecini kullanarak Remove **-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.
*Force* parametresi belirtildiğinden, komut çalışma alanını kaldırmadan önce sizi istemez.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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
Çalışma alanının adını belirtir.

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

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure Operasyonel Öngörüler cmdlet 'Leri](./AzureRM.OperationalInsights.md)

[Get-Azurermoperationalınsightsworkspace](./Get-AzureRmOperationalInsightsWorkspace.md)


