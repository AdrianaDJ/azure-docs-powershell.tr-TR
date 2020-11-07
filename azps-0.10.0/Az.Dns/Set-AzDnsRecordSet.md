---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935915"
---
# Set-AzDnsRecordSet

## SYNOPSIS
DNS kayıt kümesini güncelleştirir.

## INDEKI

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzDnsRecordSet** cmdlet 'i, yerel bir **RECORDSET** nesnesinden Azure DNS hizmetinde bir kayıt güncelleştirir.

Bir **Recordset** nesnesini parametre olarak veya Pipeline işlecini kullanarak geçirebilirsiniz.

Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.

Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmez.
Bu, eşzamanlı değişiklikler için koruma sağlar.
Bu davranışı, yinelenen değişikliklerden bağımsız olarak kayıt kümesini güncelleştiren, *overwrite* parametresini kullanarak kaldırabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: kayıt kümesini güncelleştirme
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

İlk komut, Get-AzDnsRecordSet cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar.

İkinci ve üçüncü komutlar, kayıt kümesine iki kayıt eklemek için satır dışı operasyonlardır.

Final komutu, güncelleştirmeyi kaydetmek için **set-AzDnsRecordSet** cmdlet 'ini kullanır.

### Örnek 2: SOA kaydını güncelleştirme
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

İlk komut, **Get-AzDnsRecordset** cmdlet 'ini kullanarak belirtilen kayıt kümesini alır ve ardından $Recordset değişkeninde depolar.

İkinci komut $RecordSet 'da belirtilen SOA kaydını güncelleştirir.

Son komutu, $RecordSet güncelleştirmeyi yaymak için **set-AzDnsRecordSet** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -Overwrite
Yinelenen değişikliklere bakılmaksızın kayıt kümesinin güncelleştirileceğini gösterir.

Yerel **kayıt** kümesi nesnesi alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi güncelleştirilmeyecek.
Bu, eşzamanlı değişiklikler için koruma sağlar.
Bu davranışı bastırmak için, *üzerine yazma* parametresini kullanarak, yinelenen değişikliklere bakılmaksızın kayıt kümesi güncellenir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kayıt kümesi
Güncelleştirilecek **kayıt kümesini** belirtir.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Bir **Recordset** nesnesini bu cmdlet 'e geçirebilirsiniz.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Bu cmdlet, güncelleştirilmiş **Recordset** nesnesini temsil eden bir nesne döndürür.

## NOTLARıNDA
*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.
Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.

*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.
*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez. 

## ILGILI BAĞLANTıLAR

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
