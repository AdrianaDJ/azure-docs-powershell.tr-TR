---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 42454d41281746e4b95399e74aa4cb7a9c3c7a77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752022"
---
# Set-AzDnsZone

## SYNOPSIS
DNS bölgesinin özelliklerini güncelleştirir.

## INDEKI

### Alanlar (varsayılan)
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nesnelerini
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
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

### Örnek 3: KIMLIĞINI belirterek özel bir bölgeyi sanal bir ağla Ilişkilendirme
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

Bu komut, KIMLIĞI belirterek özel DNS bölgesini bir kayıt ağı olarak myvnet myprivatezone.com ile ilişkilendirir.

### Örnek 4: ağ nesnesini belirterek özel bir bölgeyi sanal bir ağla Ilişkilendirme.
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

Bu komut, $vnet değişkeni ile temsil edilen sanal ağ nesnesini Set-AzDnsZone cmdlet 'ine geçirerek, özel DNS bölgesini bir kayıt ağı olarak myvnet ile ilişkilendirir.

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
Güncelleştirilecek DNS bölgesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Registrationvirtualnetworkıd
Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Bu DNS bölgesindeki kayıtları çözümleyebileceğiniz sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resolutionvirtualnetworkıd
Bu DNS bölgesindeki kayıtları çözümleyemeyecek sanal ağ kimliklerinin listesi, yalnızca özel bölgeler için kullanılabilir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Güncelleştirilecek bölgeyi içeren kaynak grubunun adını belirtir.
Ayrıca, BölgeAdı parametresini de belirtmeniz gerekir.
Alternatif olarak, bölgeyi *bölge* parametresi veya ardışık düzene sahip bir dnsZone nesnesi kullanarak belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
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
Type: Microsoft.Azure.Commands.Dns.DnsZone
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
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### System. topluluklar. Hashtable

### System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### Microsoft. Azure. Commands. DNS. DnsZone

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsZone

## NOTLARıNDA
*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.
Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.
*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.
*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.

## ILGILI BAĞLANTıLAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[Yeni-Azdnzone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
