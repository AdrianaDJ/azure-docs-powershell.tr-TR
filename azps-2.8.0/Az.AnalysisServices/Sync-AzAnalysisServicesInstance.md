---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 2c7162f5a93c112a3f67b308941b56b698792fa3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753625"
---
# Sync-AzAnalysisServicesInstance

## SYNOPSIS

Belirtilen Analysis Services Server örneğindeki belirli bir veritabanını, geçerli olarak oturum açmış olan ortamdaki tüm sorgu ölçeği örneklerinin Add-AzAnalysisServicesAccount komutta belirtildiği gibi eşitler

## INDEKI

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım

Sync-AzAnalysisServicesInstance cmdlet 'i, Analysis Services sunucusundaki belirtilen bir veritabanını Add-AzAnalysisServicesAccount komutunda belirtilen geçerli olarak oturum açmış ortamdaki tüm sorgu ölçeği örneklerine eşitler

## ÖRNEKLERDEN

### Örnek 1

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Bu komut, Add-AzAnalysisServicesAccount komutunu kullanarak Kullanıcı bu ortamda oturum açmış olduğundan westus.asazure.windows.net ortamdaki ' contoso ' adlı sunucudaki SalesOrders adlı veritabanını eşitler.

## PARAMETRELERINE

### -Veritabanı

Eşitlenecek veritabanının kimliği

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Örnek

Yeniden başlatılacak Analysis Services sunucusu örneğinin adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AnalysisServices. Datadüzlemi. model. ScaleOutServerDatabaseSyncDetails

## NOTLARıNDA

Diğer ad: Sync-AzAsInstance

## ILGILI BAĞLANTıLAR
