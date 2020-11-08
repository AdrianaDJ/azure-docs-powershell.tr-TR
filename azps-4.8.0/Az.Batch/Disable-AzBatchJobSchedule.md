---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107908"
---
# Disable-AzBatchJobSchedule

## SYNOPSIS
Toplu iş çizelgesini devre dışı bırakır.

## INDEKI

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Disable-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini devre dışı bırakır.
Bir zamanlamayı devre dışı bırakırsanız, işler bu zamanlamaya göre oluşturulmaz.
Devre dışı bir zamanlamayı daha sonra etkinleştirebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: iş çizelgesini devre dışı bırakma
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını devre dışı bırakır.
$Context değişkenine bağlam atamak için **Get-AzBatchAccountKey** cmdlet 'ini kullanın.

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

### -ID
Bu cmdlet 'in devre dışı olduğu iş zamanlamasının KIMLIĞINI belirtir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Enable-Azbatchjobzamanlama](./Enable-AzBatchJobSchedule.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-Azbatchjobplan](./Get-AzBatchJobSchedule.md)

[Yeni-Azbatchjobplanlama](./New-AzBatchJobSchedule.md)

[Remove-Azbatchjobplan](./Remove-AzBatchJobSchedule.md)

[Stop-Azbatchjobzamanlama](./Stop-AzBatchJobSchedule.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/Az.Batch/)
