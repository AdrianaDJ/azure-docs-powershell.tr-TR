---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 9be5ca678b690400e044b9627fd455ea2cbc29c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760899"
---
# Get-AzDnsZone

## SYNOPSIS
DNS bölgesi alır.

## INDEKI

### Varsayılan (varsayılan)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Kaynak
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzDnsZone** cmdlet 'i, belirtilen kaynak grubundan bir etki alanı adı SISTEMI (DNS) bölgesi alır.
*Name* parametresini belirtirseniz, tek bir **dnsZone** nesnesi döndürülür.
*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki tüm bölgeleri içeren bir dizi döndürülür.
Bölgeyi güncelleştirmek için **dnsZone** nesnesini kullanabilirsiniz; Örneğin, buna **kayıt kümesi** nesneleri ekleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: bölge alma
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Bu örnekte, myzone.com adlı DNS bölgesi belirtilen kaynak grubundan alınır ve $Zone değişkeninde depolanır.

### Örnek 2: kaynak grubundaki tüm bölgeleri alma
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Bu örnekte, belirtilen kaynak grubundaki tüm DNS bölgeleri alınır ve $Zones değişkeninde depolanır.

### Örnek 3: abonelikteki tüm bölgeleri alma
```
PS C:\> $Zones = Get-AzDnsZone
```

Bu örnekte, geçerli Azure aboneliğindeki tüm DNS bölgeleri alınır ve ardından $Zones değişkeninde depolanır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsZone

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azdnzone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
