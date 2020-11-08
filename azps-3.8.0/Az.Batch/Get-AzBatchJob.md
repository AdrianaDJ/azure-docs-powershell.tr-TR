---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 5b1eec59b0466dd34908d82938d0a7b4f8d99421
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107310"
---
# Get-AzBatchJob

## SYNOPSIS
Toplu iş hesabı veya iş zamanlaması için toplu işleri alır.

## INDEKI

### ODataFilter (varsayılan)
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Kimliğe
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzBatchJob** cmdlet 'ı, *batchaccountcontext* parametresinde belirtilen toplu hesap için Azure toplu işlemlerini alır.
Tek bir iş almak için *ID* parametresini kullanabilirsiniz.
Açık bir veri Protokolü (OData) filtresiyle eşleşen işleri almak için *Filter* parametresini kullanabilirsiniz.
İş zamanlaması KIMLIĞI veya **Pschoparlör Iş zamanlaması** örneği sağlarsanız, bu cmdlet yalnızca bu iş zamanlamalarının işlerini döndürür.

## ÖRNEKLERDEN

### Örnek 1: KIMLIĞE göre bir toplu iş alın
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

Bu komut Job01 KIMLIĞINE sahip işi alır.
$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.

### Örnek 2: iş zamanlaması için tüm etkin işleri alma
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

Bu komut, iş zamanlaması için KIMLIĞI JobSchedule27 olan etkin işleri alır.

### Örnek 3: ardışık düzeni kullanarak iş zamanlamasındaki tüm işleri alır
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

Bu komut, Get-AzBatchJobSchedule cmdlet 'ini kullanarak KIMLIĞI JobSchedule27 olan iş zamanlamasını alır.
Komut, iş çizelgesini ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Komut bu iş zamanlaması için tüm işleri alır.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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
İşler için bir OData filtresi yan tümcesi belirtir.
Filtre belirtmezseniz, bu cmdlet toplu hesap veya iş zamanlaması için tüm işleri döndürür.

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Bu cmdlet 'in aldığı işin KIMLIĞINI belirtir.
Joker karakterler belirtemezsiniz.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobzamanlama
İşleri içeren iş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.
**Pschoparlör** nesnesi almak için Get-AzBatchJobSchedule cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Jobscheduleıd
İşleri içeren iş zamanlamasının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Döndürülecek en fazla iş sayısını belirtir.
Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.
Varsayılan değer 1000 ' dır.

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzBatchJob](./Disable-AzBatchJob.md)

[Enable-AzBatchJob](./Enable-AzBatchJob.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-Azbatchjobplan](./Get-AzBatchJobSchedule.md)

[Yeni-AzBatchJob](./New-AzBatchJob.md)

[Remove-AzBatchJob](./Remove-AzBatchJob.md)

[Stop-AzBatchJob](./Stop-AzBatchJob.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


