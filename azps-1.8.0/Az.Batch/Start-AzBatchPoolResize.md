---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: c68911de8d01a654593e72b98ba5d53bf40c76ed
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761824"
---
# Start-AzBatchPoolResize

## SYNOPSIS
Havuzu yeniden boyutlandırmaya başlar.

## INDEKI

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Start-AzBatchPoolResize** cmdlet 'i havuzda bir Azure toplu yeniden boyutlandırma işlemini başlatır.

## ÖRNEKLERDEN

### Örnek 1: bir havuzu 12 düğüme yeniden boyutlandırma
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

Bu komut, ContosoPool06 KIMLIĞI olan havuzda yeniden boyutlandırma işlemi başlatır.
İşlemin hedefi 12 adanmış işlem düğümünüz.
$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.

### Örnek 2: ayırmayı kaldırma seçeneğini kullanarak havuzu yeniden boyutlandırma
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

Bu cmdlet, havuzu beş ayrılmış işlem düğümüne yeniden boyutlandırır.
Komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.
Komut, ardışık düzen işlecini kullanarak bu havuz nesnesini geçerli cmdlet 'e geçirir.
Komut, havuzda yeniden boyutlandırma işlemi başlatır.
Hedef beş ayrılmış işlem düğümünüz.
Komut bir saatin zaman aşımı süresini belirtir.
Komut sonlandırmaya yönelik ayırmayı kaldırma seçeneğini belirtir.

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

### -Computenodedağıtıkonumseçeneği
Bu cmdlet 'in başladığı yeniden boyutlandırma işlemi için ayırmayı kaldırma seçeneğini belirtir.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

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

### -ID
Bu cmdlet 'in yeniden boyutlandıraldığı havuzun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResizeTimeout
Yeniden boyutlandırma işlemi için zaman aşımı süresini belirtir.
Havuz, hedef boyutu şu anda bağlanamazsa, yeniden boyutlandırma işlemi durur.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TARGETTE
Hedef adanmış işlem düğümlerinin sayısı.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetLowPriorityComputeNodes
Hedef düşük öncelikli işlem düğümlerinin sayısı.

```yaml
Type: System.Nullable`1[System.Int32]
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

[Get-Aztopluaccountkeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchPool](./Get-AzBatchPool.md)

[Stop-AzBatchPoolResize](./Stop-AzBatchPoolResize.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


