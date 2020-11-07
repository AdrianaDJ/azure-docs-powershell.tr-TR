---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761884"
---
# Get-AzBatchNodeAgentSku

## SYNOPSIS
Toplu iş hesabındaki toplu Iş düğümü Aracısı SKU 'Larını alır.

## INDEKI

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzBatchNodeAgentSku** cmdlet 'i, bir Azure toplu hesabında kullanılabilen düğüm Aracısı SKU 'larını alır.
*Batchcontext* parametresini kullanarak hesabı belirtin.
Aramanızı açık bir veri Protokolü (OData) filtresiyle eşleşen STB 'ler olarak daraltabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: tüm kullanılabilir düğüm Aracısı SKU 'Larını alma
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

İlk komut, **Get-AzBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamı alır.
Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.
İkinci komut, toplu Iş desteği olan tüm kullanılabilir düğüm Aracısı SKU 'Larını alır.

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

### -Filtre
Düğüm Aracısı SKU 'Ları için bir OData filtre yan tümcesi belirtir.
Filtre belirtmezseniz, bu cmdlet toplu Işlemle desteklenen tüm düğüm Aracısı SKU 'Larını döndürür.

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

### -MaxCount
Döndürülecek düğüm Aracısı SKU sayısının üst sınırını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSNodeAgentSku

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Aztopluaccountkeys](./Get-AzBatchAccountKey.md)


