---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935911"
---
# Set-AzDnsZone

## SYNOPSIS
DNS bölgesinin özelliklerini güncelleştirir.

## INDEKI

### Alanlardır
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Nesnelerini
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzDnsZone** cmdlet 'ı, Azure DNS HIZMETINDE belirtilen DNS bölgesini güncelleştirir.
Bu cmdlet, bölgedeki kayıt kümelerini güncelleştirmez.

Bir **dnsZone** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilir ya da bir alternatif olarak, *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.

Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.

DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez. Bu, eşzamanlı değişiklikler için koruma sağlar. Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: DNS bölgesini güncelleştirme
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

İlk komut, myzone.com adlı bölgeyi belirtilen kaynak grubundan alır ve $Zone değişkeninde depolar.

İkinci komut $Zone etiketlerini güncelleştirir.

Son komutu değişikliği kaydeder.

### Örnek 2: bir bölgeye ait etiketleri güncelleştirme
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Bu komut, önce bölgeyi açıkça almadan myzone.com adındaki bölgenin etiketlerini güncelleştirir.

## PARAMETRELERINE

### -Ad
Güncelleştirilecek DNS bölgesinin adını belirtir.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
DNS bölgesini nesne olarak geçirirken (bölge nesnesini veya ardışık düzen aracılığıyla), yerel DnsZone nesnesinin alındığı bu yana Azure DNS 'de değiştirilmişse bu, güncelleştirilmez. Bu, eşzamanlı değişiklikler için koruma sağlar. Bu *davranışı, eş* zamanlı değişikliklerden bağımsız olarak, bölgeyi güncelleyen parametreyle kaldırabilirsiniz.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.
Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.

Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bölge
Güncelleştirilecek DNS bölgesini belirtir.

Alternatif olarak, bölgeyi *BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak belirtebilirsiniz.

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. DNS. DnsZone
Bir DnsZone nesnesini bu cmdlet 'e boru edebilirsiniz.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsZone
Bu cmdlet, yeni ETag ile güncelleştirilmiş DNS bölgesini temsil eden bir DnsZone nesnesi döndürür.

## NOTLARıNDA
*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.
Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.

*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.
*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.

## ILGILI BAĞLANTıLAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[Yeni-Azdnzone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)