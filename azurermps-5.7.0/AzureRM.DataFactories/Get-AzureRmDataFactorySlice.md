---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586744"
---
# Get-AzureRmDataFactorySlice

## SYNOPSIS
Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDataFactorySlice** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.
Görüntülenecek bir veri dilimleri aralığı tanımlamak için başlangıç saati ve bitiş saati belirtin.

Veri diliminin durumu aşağıdaki değerlerden biridir: 

- PendingExecution.
Veri işleme başlamadı. 
- Progress.
Veri işleme sürüyor. 
- Çalıştırılmaya.
Veri işleme tamamlandı.
Veri dilimi, bağımlı dilimlerin kullanması için hazırdır. 
- Erişilemedi.
Dilimi üreten çalışma başarısız oldu. 
- Git.
Veri Fabrikası dilimin işlenmesini atlar. 
- Yeniden deneyin.
Veri Fabrikası dilimi üreten çalıştırmayı yeniden dener. 
- Zaman aşımına uğradı. Veri işleme zaman aşımına uğradı. 
- PendingValidation.
Veri dilimi işlenmeden önce doğrulamayı bekliyor. 
- Doğrulamayı yeniden deneyin.
Veri Fabrikası dilimin doğrulamasını yeniden dener. 
- Doğrulanamadı.
Dilim doğrulanamadı.

Dilimlerin her biri için Get-AzureRmDataFactoryRun cmdlet 'ini kullanarak dilimi üreten çalışma hakkında daha fazla bilgi görebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: veri kümesi veri dilimlerini alma
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Bu komut, wikiadf adlı veri fabrikası 'ndaki wikiaggreg
Komut, StartDateTime parametresi belirttiğinde üretilen dilimleri alır.
Aşağıdaki örnek kod, bu DataSet 'in kullanılabilirliğini JavaScript nesne gösterimi (JSON) dosyasının her saati olarak ayarlar.

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
Hazır dilimler zaten çalıştırıldı.
Bekleyen dilimler, Set-AzureRmDataFactoryPipelineActivePeriod cmdlet 'inin belirttiği aralıktaki her saatin sonunda çalıştırılmasını beklemektedir.
Bu örnekte, ardışık düzen ve dilimin başlangıç ve bitiş dönemleri bir gün değeri (24 saat) olur.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Bu cmdlet 'in dilimleri aldığı veri kümesinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### -EndDateTime
Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.
Bu cmdlet, bu parametrenin belirttiği zamandan önce üretilmiş olan dilimleri alır.
**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .

*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)

Varsayılan saat dilimi göstergesi UTC.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait dilimleri alır.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.
Bu cmdlet, bu parametrenin belirttiği zamandan sonra üretilen dilimleri alır.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. Windowsazve. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Set-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Set-Azurermdatafactoryptam](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


