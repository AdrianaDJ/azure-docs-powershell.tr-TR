---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765071"
---
# Export-AzureAnalysisServicesInstance

## SYNOPSIS
Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğinden Add-AzureAnalysisServicesAccount komutunda belirtilen bir günlüğü dışarı aktarır

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## Tanım
Export-AzureAnalysisServicesInstance cmdlet 'i Azure Analysis Services sunucusundan dosyaya günlük aktarma

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamdaki günlükleri ' TestServer ' sunucusundan dışarı aktarır ve bu dosyayı OutputPath ' C:\yol\to\log\testserver.log ' dosyasında belirtilen dosyaya kaydeder

## PARAMETRELERINE

### -Örnek
Analysis Services sunucu örneğinin adı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Dışarı aktarılacak dosyanın çıkış yolu

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Varsa dosyanın üzerine yaz

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA
Diğer ad: Export-AzureAsInstanceLog

## ILGILI BAĞLANTıLAR

