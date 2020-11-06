---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588221"
---
# Sync-AzureAnalysisServicesInstance

## SYNOPSIS

Belirtilen Analysis Services Server örneğindeki belirli bir veritabanını, geçerli olarak oturum açmış olan ortamdaki tüm sorgu ölçeği örneklerinin Add-AzureAnalysisServicesAccount komutta belirtildiği gibi eşitler

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## Tanım

Sync-AzureAnalysisServicesInstance cmdlet 'i, Analysis Services sunucusundaki belirtilen bir veritabanını Add-AzureAnalysisServicesAccount komutunda belirtilen geçerli olarak oturum açmış ortamdaki tüm sorgu ölçeği örneklerine eşitler

## ÖRNEKLERDEN

### Örnek 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Bu komut, Add-AzureAnalysisServicesAccount komutu kullanarak kullanıcının bu enviroment oturum açtığı sağlanmış westus.asazure.windows.net ortamdaki ' contoso ' adlı sunucudaki SalesOrders adlı veritabanını eşitler.

## PARAMETRELERINE

### -Örnek

Yeniden başlatılacak Analysis Services sunucusu örneğinin adı

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

### -Veritabanı

Eşitlenecek veritabanının kimliği

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

### -Geçiş

Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

Diğer ad: Sync-AzureAsInstance

## ILGILI BAĞLANTıLAR
