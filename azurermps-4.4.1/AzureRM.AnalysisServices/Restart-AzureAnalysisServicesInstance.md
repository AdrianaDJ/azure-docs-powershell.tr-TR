---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 038c7456f849777f16ca0113d799b4ee8a16cd2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587051"
---
# Restart-AzureAnalysisServicesInstance

## SYNOPSIS
Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğini Add-AzureAnalysisServicesAccount komutunda belirtildiği gibi yeniden başlatır

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Restart-AzureAnalysisServicesInstance cmdlet 'i yeniden başlatır

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamda ' TestServer ' sunucusunu yeniden başlatır

## PARAMETRELERINE

### -Örnek
Yeniden başlatılacak Analysis Services sunucusu örneğinin adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA
Diğer ad: Restart-AzureAsInstance

## ILGILI BAĞLANTıLAR

