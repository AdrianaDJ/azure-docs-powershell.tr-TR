---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587687"
---
# Get-AzureBatchTaskCounts

## SYNOPSIS
Belirtilen iş için görev sayılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Kimliğe
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### ParentObject
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## Tanım
**Get-AzureBatchTaskCounts** cmdlet 'ı bir toplu Iş Için Azure Batch görevlerinin sayımını alır.
İş veya *iş* *parametresinden bir* iş belirtin.
Görev sayımları etkin, çalışan veya tamamlanan görev durumuna göre görevlerin sayısını ve başarılı veya başarısız olan görevlerin sayısını sağlar. Hazırlık durumundaki görevler çalışıyor olarak sayılır. ValidationStatus doğrulanırsa, toplu Iş hizmeti durum sayılarını liste görevleri API 'sinde bildirilen görev durumlarına göre denetleyememiştir. İş 200.000 ' den fazla görev içeriyorsa doğrulama durumu geçersiz olabilir.

## ÖRNEKLERDEN

### Örnek 1: KIMLIĞE göre görev sayımları alma
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Bu komut, iş Job01 için görev sayılarını alır.
$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

## PARAMETRELERINE

### -BatchContext
Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.
BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.
Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.
Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.
Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Job
Bu cmdlet 'in aldığı görevleri içeren işi belirtir.
Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Görev sayılarının alınacağı işin kimliği.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String
Microsoft.Azure.Commands.Batch. Modeller. Pscbalajob Microsoft.Azure.Commands.Batch.BatchAccountContext


## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSTaskCounts


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)
