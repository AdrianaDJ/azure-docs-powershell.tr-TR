---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 9b8da32a336b0320f8ca69b6f6e09d584315d0d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760290"
---
# New-AzPublicIpAddress

## SYNOPSIS
Genel bir IP adresi oluşturur.

## INDEKI

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**New-Azpublicıpaddress** cmdlet 'i genel bir IP adresi oluşturur.

## ÖRNEKLERDEN

### 1: yeni bir genel IP adresi oluşturma
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur. -AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir. ' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir.

### 2: ters FQDN ile genel IP adresi oluşturma
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

Bu komut yeni bir genel IP adresi kaynağı oluşturur. -Smartfqdn parametresiyle, bu kaynağa tahsis edilen genel IP adresi için, komutta belirtilen $customFqdn işaret eden bir DNS PTR kaydı (ters arama) oluşturulur. Önkoşul olarak, $customFqdn (say webapp.contoso.com), $dnsPrefix. $location. cloudapp.azure.com 'e işaret eden bir DNS CNAME kaydı (ileriye-arama) içermelidir.

### 3: ıptag ile yeni bir genel IP adresi oluşturun
```
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur. -AllocationMethod ' static ' olarak belirtildiğinden, genel bir IP adresi hemen bu kaynağa tahsis edilir. ' Dinamik ' olarak belirtilirse, genel IP adresi yalnızca ilişkili kaynağı (veya siz bir VM veya yük dengeleyicisi gibi) başlattığınızda tahsis edilir. Kaynak ile ilişkilendirilmiş etiketleri için ıptag kullanılır. Iptag New-AzPublicIpTag kullanarak belirtilebilir ve-ıptags aracılığıyla giriş olarak geçirilir.

### 4: önekten yeni bir genel IP adresi oluşturma
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

Bu komut yeni bir genel IP adresi kaynağı oluşturur. $DnsPrefix. $location. cloudapp.azure.com. bu kaynağın genel IP adresine işaret eden bir DNS kaydı oluşturulur. Bu kaynağa, genel bir IP adresi belirtilen Publicıpprefix 'ten hemen tahsis edilir.
Bu seçenek yalnızca ' standart ' SKU ve ' static ' AllocationMethod ile desteklenir.

## PARAMETRELERINE

### -AllocationMethod
Genel IP adresinin tahsis edilmesi yöntemini belirtir.
Bu parametre için kabul edilebilir değerler: statik veya dinamik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DomainNameLabel
Genel bir IP adresi için göreli DNS adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Idfaizzamansayısı
Bekleme süresini dakika cinsinden belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
IP adresinin sürümünü belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipetiketi
Iptag listesi.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Genel IP adresi oluşturacağınız bölgeyi belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu ortak IP adresinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publicıpprefix
Genel IP adresi ayrılacak PSPublicIpPrefix öğesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Genel IP adresi oluşturacağınız kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Smarfqdn
Geriye doğru tam etki alanı adını (FQDN) belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Genel IP SKU adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bölge
Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

### Microsoft. Azure. Commands. Network. model. PSPublicIpTag []

### Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix

### System. Int32

### System. String []

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Pspublicıpaddress

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azpublicıpaddress](./Get-AzPublicIpAddress.md)

[Remove-Azpublicıpaddress](./Remove-AzPublicIpAddress.md)

[Set-Azpublicıpadresi](./Set-AzPublicIpAddress.md)
