---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935390"
---
# New-AzLoadBalancerFrontendIpConfig

## SYNOPSIS
Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.

## INDEKI

### SetByResourceSubnet
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Setbyresourceıdsubnet
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Setbyresourceidpublicıpaddress
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Setbyresourcepublicıpaddress
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.

## ÖRNEKLERDEN

### Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.

İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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
Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Privateıpaddress
Yük dengeleyicinin özel IP adresini belirtir.
Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpaddress
Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpadresisıd
Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Alt ağ
Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bölge
Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azloadbalancerfrontendıconfıg](./Add-AzLoadBalancerFrontendIpConfig.md)

[Get-Azloadbalancerfrontendıconfıg](./Get-AzLoadBalancerFrontendIpConfig.md)

[New-Azpublicıpaddress](./New-AzPublicIpAddress.md)

[Remove-Azloadbalancerfrontendıconfıg](./Remove-AzLoadBalancerFrontendIpConfig.md)

[Set-Azloadbalancerfrontendıconfıg](./Set-AzLoadBalancerFrontendIpConfig.md)


