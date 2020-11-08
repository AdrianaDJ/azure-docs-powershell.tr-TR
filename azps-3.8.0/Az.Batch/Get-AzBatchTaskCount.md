---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: f339e315f025dff921687730d9211c5b049c0f59
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107264"
---
# Get-AzBatchTaskCount

## SYNOPSIS
Belirtilen iş için görev sayılarını alır.

## INDEKI

### Kimliğe
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzBatchTaskCount** cmdlet 'ı, toplu Iş Için Azure Batch görevlerinin sayımını alır.
İş veya *iş* *parametresinden bir* iş belirtin.
Görev sayımları etkin, çalışan veya tamamlanan görev durumuna göre görevlerin sayısını ve başarılı veya başarısız olan görevlerin sayısını sağlar. Hazırlık durumundaki görevler çalışıyor olarak sayılır. ValidationStatus doğrulanırsa, toplu Iş hizmeti durum sayılarını liste görevleri API 'sinde bildirilen görev durumlarına göre denetleyememiştir. İş 200.000 ' den fazla görev içeriyorsa doğrulama durumu geçersiz olabilir.

## ÖRNEKLERDEN

### Örnek 1: KIMLIĞE göre görev sayımları alma
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Bu komut, iş Job01 için görev sayılarını alır.
$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.

## PARAMETRELERINE

### -BatchContext
Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.
BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.
Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.
Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.
Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

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

### -Job
Bu cmdlet 'in aldığı görevleri içeren işi belirtir.
Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
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
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSTaskCounts

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)
