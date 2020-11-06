---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592508"
---
# Get-AzureRmDnsRecordSet

## SYNOPSIS
DNS kayıt kümesi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Alanlardır
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Nesnelerini
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDnsRecordSet** cmdlet 'i belirtilen ad ve türüyle belirtilen bölgedeki etki alanı adı SISTEMI (DNS) kayıt kümesini alır.

*Name* veya *RecordType* parametrelerini belirtmezseniz, bu cmdlet bölgedeki belirtilen türdeki tüm kayıt kümelerini döndürür.
*Kayıt türü* parametresini belirtirseniz ancak *Name* parametresini belirtmezseniz, bu cmdlet belirtilen kayıt türünün tüm kayıt kümelerini döndürür.

Bu cmdlet 'e bir **dnsZone** nesnesi geçirmek için Pipeline işlecini kullanabilir veya bir **dnsZone** nesnesini *bölge* parametresi olarak geçirebilirsiniz ya da bölge ve kaynak grubunu adıyla belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: belirtilen ad ve türde kayıt kümelerini alma
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Bu komut, kayıt türü kayıt kümesini belirtilen kaynak grubu ve bölgesinde alır ve $RecordSet değişkeninde depolar.
*Name* ve *RecordType* parametreleri belirtildiğinden, yalnızca bir **Recordset** nesnesi döndürülür.

### Örnek 2: belirtilen türde kayıt kümelerini alma
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Bu komut MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki kayıt türü kayıt kümesinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.

### Örnek 3: bölgedeki tüm kayıt kümelerini alma
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Bu komut, MyResourceGroup adındaki kaynak grubundaki myzone.com adlı bölgedeki tüm kayıt kümelerinin bir dizisini alır ve ardından $RecordSets değişkeninde depolar.

### Örnek 4: DnsZone nesnesini kullanarak bölgedeki tüm kayıt kümelerini alma
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

Bu örnek, yukarıdaki örnek 3 ile eşdeğerdir.
Bu kez bölge, bölge nesnesi kullanılarak belirtilir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Ad
Alınacak **kayıt kümesinin** adını belirtir.
*Name* parametresini belirtmezseniz, belirtilen türdeki tüm kayıt kümeleri döndürülür.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Bu cmdlet 'in aldığı DNS kaydının türünü belirtir.

Geçerli değerler: 

- Bir
- AAAA
- KAYDıNı
- DOSYASıNA
- Seç
- PTR
- SOA
- SRV
- ,

*RecordType* parametresini belirtmezseniz, *ad* parametresini de atlayabilirsiniz. Bu cmdlet, bölgedeki tüm kayıt kümelerini (tüm adlarda ve türlerinde) döndürür.

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
DNS bölgesini içeren kaynak grubunu belirtir.
Bölge adı da belirtilmelidir ve *BölgeAdı* da belirtilmelidir.

Alternatif olarak, bölge parametresini kullanarak bir **dnsZone** nesnesini *geçirerek bölgeyi ve* kaynak grubunu belirtebilirsiniz.

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
Bu cmdlet 'in aldığı kayıt kümesini içeren DNS bölgesini belirtir.
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

### -BölgeAdı
Alınacak kayıt kümesini içeren DNS bölgesinin adını belirtir.
Bölgeyi içeren kaynak grubunun da belirtilmesi için, *Resourcegroupname* parametresi kullanılır.

Alternatif olarak, bölge ve kaynak grubunu, *bölge* parametresini kullanarak bir DNS bölgesi nesnesini geçirerek belirtebilirsiniz.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. DNS. DnsZone
Bir **dnsZone** nesnesini bu cmdlet 'e boru edebilirsiniz.
**DnsZone** nesnesi, **kayıt kümesi** nesnesinin bakılacak bölgeyi temsil eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Bu cmdlet, bulunan kayıt kümelerini temsil eden bir veya birden çok nesne döndürür.
*Name* ve *RecordType* parametreleri belirtilirse, birden çok **Recordset** nesnesi dizi olarak döndürülürsünüz **.**

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


