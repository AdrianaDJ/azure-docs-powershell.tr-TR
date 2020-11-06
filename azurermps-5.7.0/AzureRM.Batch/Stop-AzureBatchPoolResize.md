---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587672"
---
# Stop-AzureBatchPoolResize

## SYNOPSIS
Havuz yeniden boyutlandırma işlemini durdurur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Stop-AzureBatchPoolResize** cmdlet 'i, havuzda bir Azure toplu yeniden boyutlandırma işlemini durdurur.

## ÖRNEKLERDEN

### Örnek 1: havuzu yeniden boyutlandırmayı durdurma
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

Bu komut, ContosoPool06 KIMLIĞINE sahip havuzda yeniden boyutlandırma işlemini durdurur.
$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

### Örnek 2: ardışık düzeni kullanarak havuzu yeniden boyutlandırmayı durdurma
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

Bu komut, ardışık düzen işlecini kullanarak havuzu yeniden boyutlandırmayı durdurur.
Komut, Get-AzureBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.
Komut bu havuz nesnesini geçerli cmdlet 'e geçirir.
Komut bu havuzda yeniden boyutlandırma işlemini durdurur.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: BatchAccountContext
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Bu cmdlet 'in yeniden boyutlandırma işlemini durdurduğu havuzun KIMLIĞINI belirtir.

```yaml
Type: String
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

### BatchAccountContext
' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder

### Dizisi
' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Start-AzureBatchPoolResize](./Start-AzureBatchPoolResize.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)


