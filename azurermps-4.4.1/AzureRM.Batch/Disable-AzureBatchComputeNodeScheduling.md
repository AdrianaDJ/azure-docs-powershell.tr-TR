---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593594"
---
# Disable-AzureBatchComputeNodeScheduling

## SYNOPSIS
Belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Kimlik (varsayılan)
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Disable-AzureBatchComputeNodeScheduling** cmdlet 'i belirtilen COMPUTE düğümündeki görev zamanlamasını devre dışı bırakır.
Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.
Bir işlem düğümündeki görev zamanlamasını devre dışı bıraktıktan sonra, düğümün görev sırasındaki işlere ne yapabileceğinizi belirleme seçeneğiniz de vardır.
**Disable-AzureBatchComputeNodeScheduling** şunları yapmanızı sağlar: 

- Görevleri sonlandırın ve iş kuyruğuna geri yerleştirin.
Bu, bu görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar. 
- Görevleri sonlandırın ve iş kuyruğundan kaldırın.
Bu şekilde durdurulan görevler yeniden planlanamaz. 
- Yürütülmekte olan tüm görevlerin tamamlanmasını bekleyin ve ardından işlem düğümündeki görev zamanlamasını devre dışı bırakın. 
- Tüm çalışan görevlerin tamamlanmasını bekleyin ve tüm veri bekletme dönemleri, işlem düğümündeki görev zamanlamasını devre dışı bırakın.

## ÖRNEKLERDEN

### Örnek 1: işlem düğümündeki görev zamanlamasını devre dışı bırakma
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Bu komutlar, COMPUTE düğümü TVM-1783593343_34-20151117t222514z.
Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.

İkinci komut daha sonra bu nesne başvurusunu ve **Disable-AzureBatchComputeNodeScheduling** cmdlet 'ini kullanarak Pool myvm-1783593343_34-20151117t222514z.

*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, şu anda COMPUTE düğümünde çalışan tüm görevler requeued olacaktır.

### Örnek 2: havuzdaki tüm işlem düğümlerinde görev zamanlamasını devre dışı bırakma
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

Bu komutlar, toplu iş havuzu Pool06 tüm bilgisayar düğümlerinde görev zamanlamasını devre dışı bırakır.
Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.

Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzureBatchComputeNode** .
Bu koleksiyon daha sonra, koleksiyondaki her işlem düğümündeki görev zamanlamasını devre dışı bırakmak için **-AzureBatchComputeNodeScheduling** cmdlet 'ine gönderilir.

*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, işlem düğümlerinde çalışmakta olan tüm görevler requeued olacaktır.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

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
Bu nesne başvurusu, Get-AzureBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.

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

### BatchAccountContext
' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder

### PSComputeNode
' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Enable-AzureBatchComputeNodeScheduling](./Enable-AzureBatchComputeNodeScheduling.md)


