---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 836ad4cda6d6631baf0885ac0ec380fdc401fde6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761853"
---
# New-AzBatchJobSchedule

## SYNOPSIS
Toplu Iş hizmetinde iş çizelgesi oluşturur.

## INDEKI

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-Azbatchjobzamanlama** cmdlet 'ı Azure Batch hizmetinde bir iş zamanlaması oluşturur.
*Batchaccountcontext* parametresi bu cmdlet 'in zamanlamayı oluşturduğu hesabı belirtir.

## ÖRNEKLERDEN

### Örnek 1: iş zamanlaması oluşturma
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

Bu örnek bir iş zamanlaması oluşturur.
İlk beş komut **Psschedule** , **Psjobspecification** ve **pspoolınformation** nesnelerini oluşturur ve değiştirir.
Komutlar New-Object cmdlet 'ini ve standart Azure PowerShell söz dizimini kullanır.
Komutlar, $Schedule ve $JobSpecification değişkenlerinde bu nesneleri depolar.
Son komut JobSchedule17 KIMLIĞINE sahip bir iş zamanlaması oluşturur.
Bu zamanlama bir günde yinelenme aralığına sahip işler oluşturur.
İşler, beşinci komutta belirtildiği gibi, ContosoPool06 KIMLIĞINE sahip havuzda çalışır.
$Context değişkenine bağlam atamak için **Get-AzBatchAccountKeys** cmdlet 'ini kullanın.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

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

### -DisplayName
İş zamanlaması için bir görünen ad belirtir.

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
Bu cmdlet 'in oluşturduğu iş zamanlamasının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobSpecification
Bu cmdlet 'in iş zamanlamasına eklediği işlerin ayrıntılarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
İş zamanlamasına eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.
Anahtar, meta veri adıdır.
Değer, meta veri değeridir.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zamanlama
Ne zaman iş oluşturulacağını belirleyen zamanlamayı belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-Azbatchjobzamanlama](./Disable-AzBatchJobSchedule.md)

[Enable-Azbatchjobzamanlama](./Enable-AzBatchJobSchedule.md)

[Get-Aztopluaccountkeys](./Get-AzBatchAccountKey.md)

[Get-Azbatchjobplan](./Get-AzBatchJobSchedule.md)

[Remove-Azbatchjobplan](./Remove-AzBatchJobSchedule.md)

[Stop-Azbatchjobzamanlama](./Stop-AzBatchJobSchedule.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


