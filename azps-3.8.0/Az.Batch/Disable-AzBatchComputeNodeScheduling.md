---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937876"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.

## INDEKI

### Kimlik (varsayılan)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Disable-AzBatchComputeNodeScheduling** cmdlet 'i belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.
Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.
Bir işlem düğümündeki görev zamanlamasını devre dışı bıraktıktan sonra, düğümün görev sırasındaki işlere ne yapabileceğinizi belirleme seçeneğiniz de vardır.
**Disable-AzBatchComputeNodeScheduling** aşağıdakileri yapmanızı sağlar: 
- Görevleri sonlandırın ve iş kuyruğuna geri yerleştirin.
Bu, bu görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar. 
- Görevleri sonlandırın ve iş kuyruğundan kaldırın.
Bu şekilde durdurulan görevler yeniden planlanamaz. 
- Yürütülmekte olan tüm görevlerin tamamlanmasını bekleyin ve ardından işlem düğümündeki görev zamanlamasını devre dışı bırakın. 
- Tüm çalışan görevlerin tamamlanmasını bekleyin ve tüm veri bekletme dönemleri, işlem düğümündeki görev zamanlamasını devre dışı bırakın.

## ÖRNEKLERDEN

### Örnek 1: işlem düğümündeki görev zamanlamasını devre dışı bırakma
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Bu komutlar, COMPUTE düğümü TVM-1783593343_34-20151117t222514z.
Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.
İkinci komut daha sonra bu nesne başvurusunu ve **Disable-AzBatchComputeNodeScheduling** cmdlet 'ini kullanarak havuz myvm-1783593343_34-20151117t222514z.
*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, şu anda COMPUTE düğümünde çalışan tüm görevler requeued olacaktır.

### Örnek 2: havuzdaki tüm işlem düğümlerinde görev zamanlamasını devre dışı bırakma
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Bu komutlar, toplu iş havuzu Pool06 tüm bilgisayar düğümlerinde görev zamanlamasını devre dışı bırakır.
Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.
Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzBatchComputeNode** .
Bu koleksiyon, koleksiyondaki her işlem düğümündeki görev zamanlamasını devre dışı bırakmak için **-AzBatchComputeNodeScheduling** cmdlet 'ine gönderilir.
*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, işlem düğümlerinde çalışmakta olan tüm görevler requeued olacaktır.

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

### -ComputeNode
Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümüne yönelik bir nesne başvurusu belirtir.
Bu nesne başvurusu, Get-AzBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
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

### -DisableSchedulingOption
Bu cmdlet 'in, zamanlama devre dışı bırakılmakta olan bilgisayar düğümünde çalışmakta olan tüm görevlerle nasıl ilgili olduğunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Requeue.
Görevler hemen durdurulur ve iş kuyruğuna geri döner.
Bu, görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar.
Bu varsayılan değerdir. 
- Ermesini.
Görevler hemen durdurulur ve iş sırasından kaldırılır.
Bu görevler yeniden planlanmayacaktır. 
- Görevsiz tamamlama.
İşlem düğümündeki görev zamanlama devre dışı bırakılmadan önce çalışmakta olan görevler tamamlayabilecektir.
Bu düğümde yeni görev planlanmayacaktır. 
- RetainedData.
Şu anda çalışan görevler tamamlayabilecektir ve veri bekletme dönemleri, işlem düğümündeki görev zamanlama devre dışı bırakılmadan önce sona erecek.
Bu düğümde yeni görev planlanmayacaktır.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Görev zamanlama 'nın devre dışı bırakıldığı işlem düğümünün KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.
*PoolId* parametresini kullanıyorsanız, aynı komutta *ComputeNode* parametresini kullanmayın.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


