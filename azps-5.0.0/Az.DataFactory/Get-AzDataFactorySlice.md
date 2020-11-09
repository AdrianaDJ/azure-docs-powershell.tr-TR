---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321042"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzDataFactorySlice** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır.
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
Dilimlerin her biri için Get-AzDataFactoryRun cmdlet 'ini kullanarak dilimi üreten çalışma hakkında daha fazla bilgi görebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: veri kümesi veri dilimlerini alma
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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
kullanılabilirlik: {dönem: "saat", periodMultiplier: 1} bazı sonuçlar hazır ve diğerleri de PendingExecution.
Hazır dilimler zaten çalıştırıldı.
Bekleyen dilimler, Set-AzDataFactoryPipelineActivePeriod cmdlet 'inin belirttiği aralıktaki her saatin sonunda çalıştırılmasını beklemektedir.
Bu örnekte, ardışık düzen ve dilimin başlangıç ve bitiş dönemleri bir gün değeri (24 saat) olur.

### Örnek 2

Azure Veri Fabrikası 'nde bir veri kümesi için veri dilimlerini alır. oluşturulmuş

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimleri alır.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
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
Type: System.String
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00

```yaml
Type: System.DateTime
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
Type: System.String
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
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

### System. String

## ÇıKıŞLAR

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-Azdatafactorypipelineactivedönem](./Set-AzDataFactoryPipelineActivePeriod.md)


