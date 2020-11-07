---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938635"
---
# Stop-AzBatchJobSchedule

## SYNOPSIS
Toplu iş çizelgesini durdurur.

## INDEKI

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Stop-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini durdurur.

## ÖRNEKLERDEN

### Örnek 1: iş çizelgesini durdurma
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını durdurur.
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
Bu cmdlet 'in durduğu iş zamanlamasının KIMLIĞINI belirtir.

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

[Yeni-Azbatchjobplanlama](./New-AzBatchJobSchedule.md)

[Remove-Azbatchjobplan](./Remove-AzBatchJobSchedule.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


