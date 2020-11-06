---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 067f3be3aa668ba5402881b697d7def09cb88658
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593749"
---
# New-AzureRmBatchAccountKey

## SYNOPSIS
Toplu hesap anahtarını yeniden oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmBatchAccountKey** cmdlet 'ı bir Azure toplu hesabının birincil veya ikincil anahtarını yeniden oluşturur.
Cmdlet, geçerli bir sın **Yaccountkey** ve **SecondaryAccountKey** özelliklerine sahip bir **batchaccountcontext** nesnesi döndürür.

## ÖRNEKLERDEN

### Örnek 1: bir toplu Iş hesabında birincil hesap anahtarını yeniden oluşturma
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Bu komut, pfuller adlı toplu Iş hesabındaki birincil hesap anahtarını yeniden oluşturur.

## PARAMETRELERINE

### -AccountName
Bu cmdlet 'in bir anahtarı yeniden sunduğu toplu Iş hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -KeyType
Bu cmdlet 'in yeniden kullandığı anahtar türünü belirtir.
Geçerli değerler: 

- Yararı
- İK

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in bir anahtarı yeniden sunduğu hesabın kaynak grubunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### BatchAccountContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)


