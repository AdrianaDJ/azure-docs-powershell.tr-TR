---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753186"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Belirtilen işlem düğümündeki görev zamanlamasını mümkün kılar.

## INDEKI

### Kimlik (varsayılan)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Enable-AzBatchComputeNodeScheduling** cmdlet 'i belirtilen işlem düğümündeki görev zamanlama özelliğini etkinleştirir.
Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.

## ÖRNEKLERDEN

### Örnek 1: işlem düğümündeki görev zamanlamasını etkinleştirme
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Bu komutlar, COMPUTE node TVM-1783593343_34-20151117t222514z.
Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.
İkinci komut daha sonra bu nesne başvurusunu ve **Enable-AzBatchComputeNodeScheduling** cmdlet 'ini kullanır ve myvm-1783593343_34-20151117t222514z üzerinde görev zamanlamasını etkinleştirir.

### Örnek 2: havuzdaki işlem düğümlerinde görev zamanlamasını etkinleştirme
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Bu komutlar, havuz Pool06 bulunan tüm işlem düğümlerinde görev zamanlamasını etkinleştirir.
Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.
Bu nesne başvurusu $context adlı bir değişkende depolanır.
Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzBatchComputeNode** .
Bu koleksiyon, koleksiyondaki her bir işlem düğümünde görev zamanlama **özelliğini etkinleştiren Enable-AzBatchComputeNodeScheduling** cmdlet 'ine gönderilir.

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

### -ComputeNode
Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümüne bir nesne başvurusu belirtir.
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

### -ID
Görev zamanlama özelliğinin etkinleştirildiği COMPUTE düğümünün KIMLIĞINI belirtir.

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
Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


