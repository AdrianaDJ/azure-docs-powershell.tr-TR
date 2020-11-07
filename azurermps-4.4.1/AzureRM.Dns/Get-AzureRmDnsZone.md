---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764065"
---
# Get-AzureRmDnsZone

## SYNOPSIS
DNS bölgesi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Varsayılan (varsayılan)
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Kaynak
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.
*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.
*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.
Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: bölge alma
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.

### Örnek 2: kaynak grubundaki tüm bölgeleri alma
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.

### Örnek 3: abonelikteki tüm bölgeleri alma
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.

## PARAMETRELERINE

### -Ad
Alınacak DNS bölgesinin adını belirtir.

*Name* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak GRUBUNDAKI tüm DNS bölgelerini alır.
*Resourcegroupname* parametresini de atlarsanız, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Alınacak DNS bölgesini içeren kaynak grubunun adını belirtir.

*Resourcegroupname* öğesini belirtmezseniz, *Name* parametresini de atmalısınız.
Bu durumda, bu cmdlet geçerli Azure aboneliğindeki tüm DNS bölgelerini alır.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Yabilirsiniz
Bu cmdlet girişi boru yapmanıza izin vermiyor.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsZone
Bu cmdlet, DNS bölgesini temsil eden bir nesne döndürür.
Bölge adı belirtilmezse, bölge nesneleri dizisi döndürülür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
