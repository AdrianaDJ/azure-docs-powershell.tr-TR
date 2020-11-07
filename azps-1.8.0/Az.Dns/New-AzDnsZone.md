---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760891"
---
# New-AzDnsZone

## SYNOPSIS
Yeni bir DNS bölgesi oluşturur.

## INDEKI

### Kimlikler (varsayılan)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nesnelere
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzDnsZone** cmdlet 'i, belirtilen kaynak grubunda yeni bir etki alanı adı SISTEMI (DNS) oluşturur. *Name* parametresi için BENZERSIZ bir DNS bölgesi adı belirtmelisiniz veya cmdlet hata döndürüyor. Bölge oluşturulduktan sonra, bölgede kayıt kümeleri oluşturmak için New-AzDnsRecordSet cmdlet 'ini kullanın.
Cmdlet 'in onaylamanız gerekip gerekmediğini belirlemek için *Confirm* parametresini ve $ConfirmPreference Windows PowerShell değişkenini kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: DNS bölgesi oluşturma
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Bu komut, belirtilen kaynak grubunda myzone.com adlı yeni bir DNS bölgesi oluşturur ve $Zone değişkeninde depolar.

### Örnek 2: sanal ağ kimlikleri belirterek özel bir DNS bölgesi oluşturma
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağı (ID 'sini belirterek) ile oluşturur ve ardından $Zone değişkeninde depolar.

### Örnek 3: sanal ağ nesneleri belirterek özel bir DNS bölgesi oluşturma
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

Bu komut, belirtilen kaynak grubundaki myprivatezone.com adlı yeni bir özel DNS bölgesini ilişkili bir çözünürlük sanal ağıyla ($ResVirtualNetwork değişkeni ile başvurulan) oluşturur ve $Zone değişkeninde depolar.

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
Oluşturulacak DNS bölgesinin adını belirtir.

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

### -RegistrationVirtualNetwork
Bu DNS bölgesindeki sanal makine ana bilgisayar adları kayıtlarını kaydeden sanal ağların listesi, yalnızca özel bölgeler için kullanılabilir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
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
Parameter Sets: Ids
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
Parameter Sets: Objects
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
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bölgenin oluşturulacağı kaynak grubunu belirtir.

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

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
Bölgenin türü, genel veya özel. Türü olmayan veya ortak türü olmayan bölgeler, DNS hiyerarşisinde kullanılmak üzere ortak DNS hizmet sunma düzleminde sağlanır. Özel türündeki bölgeler yalnızca ilişkili sanal ağlar kümesiyle (Bu özellik önizlemede) görünür. Bu özellik bir bölge için değiştirilemez.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

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

### System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. modeller. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### System. topluluklar. Hashtable

### System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DNS. DnsZone

## NOTLARıNDA
*Confirm* parametresini kullanarak, bu cmdlet 'in onayınızı isteyip istemediğinizi sorar.
Varsayılan olarak, $ConfirmPreference Windows PowerShell değişkeninde orta veya düşük bir değer varsa cmdlet onay ister.
*Onayla* veya *Onayla: $true* belirtirseniz, bu cmdlet çalışmadan önce onayınızı ister.
*Confirm: $false* belirtirseniz cmdlet, sizden onay istemez.

## ILGILI BAĞLANTıLAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
