---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587553"
---
# Set-AzureRmDiagnosticSetting

## SYNOPSIS
Kaynağın günlükleri ve ölçümleri ayarlarını belirler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureRmDiagnosticSetting** cmdlet 'i, belirli bir kaynağın her zaman ara ve günlük kategorisini devre dışı bırakır veya devre dışı bırakır.

Günlükler ve ölçümler belirtilen depolama hesabında depolanır.

Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.

## ÖRNEKLERDEN

### Örnek 1: kaynak için tüm ölçümleri ve günlükleri etkinleştirme
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

Bu komut, Resource01 için kullanılabilir tüm ölçümleri ve günlükleri etkinleştirmiştir.

### Örnek 2: tüm ölçümleri ve günlükleri devre dışı bırakma
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

Bu komut kaynak Resource01 tüm kullanılabilir ölçümleri ve günlükleri devre dışı bırakır.

### Örnek 3: birden çok kategoriyi etkinleştirme
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

Bu komut Category1 ve Category2 'i etkinleştirmiştir.
Tüm zaman ve diğer kategoriler aynı kalır.

### Örnek 4: zaman çizgisi ve birden çok kategoriyi etkinleştirme
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

Bu komut yalnızca Category1, Category2 ve zaman grePT1M 'yi etkinleştirmiştir.
Tüm diğer zaman graterleri ve kategorileri değiştirilmez.

## PARAMETRELERINE

### -Kategoriler
*Enabled* değerine göre etkinleştirilecek veya devre dışı bırakacak günlük kategorilerinin listesini belirtir.
Bir kategori belirtmezseniz, bu komut tüm kategorilerde çalışır.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### Özellikli
Tanılamaların etkinleştirilip etkinleştirilmeyeceğini gösterir.
Tanılamayı etkinleştirmek için $True belirtin veya tanılamayı devre dışı bırakmak için $False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Eventhubauthorizationruleıd
İ

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Kaynağın KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionEnabled
Tanılama bilgilerinin etkin olup olmadığını belirtir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Bekletme ilkesini gün olarak belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servicebusruleıd
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Storageaccountıd
Verilerin kaydedileceği depolama hesabının KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Timegrains
*Etkin* değerine göre ölçümler için etkinleştirme veya devre dışı bırakma zamanını belirtir.
Zaman çizgisi belirtmezseniz, bu komut tüm kullanılabilir zaman içinde çalışır.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -
Çalışma alanının kimliği

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)


