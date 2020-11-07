---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 6c44688bcd11b624738c299dc04c1a0cb0da9494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764901"
---
# Get-AzureBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Toplu iş hazırlığını alır ve görev durumunu bırakın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Kimlik (varsayılan)
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet 'ı bir toplu Iş Için Azure toplu iş hazırlığı ve serbest bırakma görev durumunu alır.
Bu cmdlet 'e *kimlik* parametresini veya bir **Pscses işi** örneği sağlamalısınız.

## ÖRNEKLERDEN

### Örnek 1: işin iş hazırlığı ve sürüm durumunu alma
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Bu komut, iş için iş hazırlama ve görev durumunu "test" olarak alır.
$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

### Örnek 2: filtre içeren bir işin iş hazırlama ve sürüm durumunu alma ve belirtilen
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Bu komut, "TVM-2316545714_1-20170613t201733z" düğümündeki "test" işi için iş hazırlığı ve sürüm durumunu alır ve JobPreparationTaskExecutionInformation bilgilerini yalnızca geri döndürmek için select yan tümcesini kullanır

## PARAMETRELERINE

### -BatchContext
Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.
Access tuşlarının doldurulduğuna bir BatchAccountContext nesnesi almak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Genişletme
Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.
Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtre
Bir OData filtre yan tümcesi belirtir.
Filtre belirtmezseniz, bu cmdlet iş için tüm iş hazırlığı ve sürüm görev durumunu döndürür.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Hazırlığı ve bırakma görevleri alınacak olan işin KIMLIĞINI belirtir.
Joker karakterler belirtemezsiniz.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Hazırlık ve bırakma görev durumunu almak için işi temsil eden bir **Pschoparlör iş** nesnesi belirtir.
Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Döndürülecek en yüksek iş hazırlığı ve sürüm görev durumunu gösterir.
Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.
Varsayılan değer 1000 ' dır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Select
Bir OData select yan tümcesi belirtir.
Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
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

### System. String
Microsoft.Azure.Commands.Batch. Modeller. Pscbalajob Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSJobPreparationAndReleaseTaskExecutionInformation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)
