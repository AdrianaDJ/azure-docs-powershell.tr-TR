---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
ms.openlocfilehash: b86ad0382fa7f87ac8aabb6b026b84d5a879f8ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939728"
---
# Remove-AzureRmDnsRecordSet

## SYNOPSIS
Kayıt kümesini siler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Alanlardır
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Karıştır
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nesnelerini
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Remove-AzureRmDnsRecordSet** cmdlet 'i belirtilen bölgeden belirtilen kayıt kümesini siler.
Bölge Apex otomatik olarak oluşturulan SOA veya ad sunucusu (NS) kayıtlarını silemezsiniz.

Bir **Recordset** nesnesini, ardışık düzen işlecini veya parametre olarak bu cmdlet 'e geçirebilirsiniz.
Ad ve kayıt **kümesi** **nesnesi kullanmadan** bir kayıt kümesi tanımlamak için, bu cmdlet 'e, ardışık düzen işlecini veya parametre olarak kullanarak bölgeyi Bu cmdlet 'e geçirmelisiniz ya da *BölgeAdı* ve *resourcegroupname* parametrelerini belirtebilirsiniz.

Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için Confirm parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.

Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.
Bu, eşzamanlı değişiklikler için koruma sağlar.
Bunu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen *overwrite* parametresini kullanarak kaldırabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: kayıt kümesini kaldırma
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

İlk komut belirtilen kayıt kümesini alır ve $RecordSet değişkeninde depolar. İkinci komut $RecordSet 'da kayıt kümesini kaldırır.

### Örnek 2: kayıt kümesini kaldırma ve tüm onayı gösterme
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

İlk komut belirtilen kayıt kümesini alır.

İkinci komut, bu arada değişmiş olsa bile kayıt kümesini siler.
Onay istemlerinin bastırılması

## PARAMETRELERINE

### -Force
Bu parametre bu cmdlet için onaylanmaz.
Gelecek sürümde kaldırılacaktır.

Bu cmdlet 'in onaylamanız gerekip gerekmediğini denetlemek için, *Confirm* parametresini kullanın.

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

### -Ad
Kaldırılacak **kayıt kümesinin** adını belirtir.
Ada göre kayıt kümesi belirtildiğinde, DNS bölgesi, *bölge* parametresi veya *BölgeAdı* ve *resourcegroupname* parametreleri kullanılarak belirtilmelidir.

Alternatif olarak, kayıt kümesi, *Recordset* parametresi kullanılarak geçirilen bir **Recordset** nesnesi kullanılarak belirtilebilir.

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Kayıt **kümesini kayıt kümesi nesnesi kullanarak** belirtirken, yerel **kayıt** kümesi NESNESI alındıktan sonra Azure DNS 'de değiştirilmişse kayıt kümesi silinmez.
Bu, eşzamanlı değişiklikler için koruma sağlar.
Bu, yinelenen değişikliklerden bağımsız olarak kayıt kümesini silen, *overwrite* parametresi kullanılarak bastırılabilir.

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

### -Geçiş
geçiş

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
Kaldırılacak **kayıt kümesi** nesnesini belirtir.

Alternatif olarak, kayıt kümesi *ad* ve *bölge* parametreleri kullanılarak veya *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtilebilir.

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
DNS kaydı türünü belirtir.

Geçerli değerler:

- Bir
- AAAA
- KAYDıNı
- DOSYASıNA
- Seç
- PTR
- SRV
- ,

SOA kayıtları bölge silindiğinde otomatik olarak silinir.
SOA kayıtlarını el ile silemezsiniz.

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Silinecek **kayıt kümesini** içeren DNS bölgesini içeren kaynak grubunu belirtir.
Bu parametre yalnızca, kayıt kümesi ve DNS bölgesi ad ve *BölgeAdı* kullanılarak belirtildiğinde uygulanabilir *Name* .

Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *ad* ve *bölge* parametrelerini kullanarak belirtebilirsiniz.

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

### -Bölge
Silinecek **kayıt kümesini** içeren DNS bölgesini belirtir.
Bu parametre yalnızca *Name* parametresi kullanılarak kayıt kümesi belirtildiğinde uygulanabilir.

Alternatif olarak, kayıt *kümesini kayıt kümesi parametresini veya* *Name, BölgeAdı* ve *resourcegroupname* parametrelerini kullanarak *ZoneName* belirtebilirsiniz.

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BölgeAdı
Silinecek **kayıt kümesini** içeren bölgenin adını belirtir.
*Name* ve *resourcegroupname* parametrelerini de belirtmeniz gerekir.

Alternatif olarak, kayıt kümesi, kayıt *kümesi* parametresi veya *ad* ve *bölge* parametreleriyle belirtilebilir.

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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Bir **Recordset** nesnesini bu cmdlet 'e boru yapabilirsiniz.

## ÇıKıŞLAR

### Yabilirsiniz
Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA
*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.
Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.

*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.
*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.

## ILGILI BAĞLANTıLAR

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
