---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 09e2d3effbe99c6f0f126b0665330b077f27af80
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761854"
---
# New-AzBatchJob

## SYNOPSIS
Toplu Iş hizmetinde bir iş oluşturur.

## INDEKI

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzBatchJob** cmdlet 'ı, *batchaccountcontext* parametresiyle belirtilen hesapta Azure Batch hizmetinde bir iş oluşturur.

## ÖRNEKLERDEN

### Örnek 1: iş oluşturma
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

İlk komut, New-Object cmdlet 'ini kullanarak bir **Pspoolınformation** nesnesi oluşturur.
Komut bu nesneyi $PoolInformation değişkeninde depolar.
İkinci komut Pool22 KIMLIĞINE $PoolInformation nesnenin **PoolId** özelliğine atar.
Son komut ContosoJob35 KIMLIĞINE sahip bir iş oluşturur.
İş 'e eklenen Pool22 KIMLIĞI olan havuzda çalışır.
$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.

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

### -CommonEnvironmentSettings
Anahtar/değer çiftleri olarak, bu cmdlet işin projedeki tüm görevler için ayarladığı ortak ortam değişkenlerini belirtir.
Anahtar, ortam değişkeni adıdır.
Değer, ortam değişkeni değeridir.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kısıtlamalar
İş için yürütme kısıtlamalarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
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
İşin görünen adını belirtir.

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
İş için bir KIMLIK belirtir.

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

### -JobManagerTask
Iş Yöneticisi görevini belirtir.
İş başladığında toplu iş hizmeti Iş Yöneticisi görevini çalıştırır.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobPreparationTask
Iş hazırlığı görevini belirtir.
Toplu Iş hizmeti, bu işlem düğümündeki herhangi bir görevi başlatmadan önce işlem düğümündeki Iş hazırlık görevini çalıştırır.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobReleaseTask
Iş sürümü görevini belirtir.
Toplu iş hizmeti iş sona erdiğinde Iş sürümü görevini çalıştırır.
Toplu iş hizmeti, işin her görevi çalıştırdığı her işlem düğümündeki Iş sürümü görevini çalıştırır.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
İş 'e eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.
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

### -'Alltaskscomplete
İşteki tüm görevlerin tamamlandı durumunda olması durumunda, toplu Iş hizmeti 'nin aldığı eylemi belirtir.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -'Taskfailure
Bir eylem belirtir projedeki herhangi bir görev başarısız olduğunda toplu Iş hizmeti sürer.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Poolınformation
Toplu Iş hizmetinin işin görevlerini çalıştırdığı havuzun ayrıntılarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öncelik
İşin önceliğini belirtir.
Geçerli değerler:-1000 ile 1000 arasındaki tamsayılar.
-1000 değeri en düşük önceliktir.
1000 değeri en yüksek önceliktir.
Varsayılan değer 0 ' dır.

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

### -UsesTaskDependencies
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzBatchJob](./Disable-AzBatchJob.md)

[Enable-AzBatchJob](./Enable-AzBatchJob.md)

[Get-Aztopluaccountkeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-Azbatchjobplan](./Get-AzBatchJobSchedule.md)

[Remove-AzBatchJob](./Remove-AzBatchJob.md)

[Stop-AzBatchJob](./Stop-AzBatchJob.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


