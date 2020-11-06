---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8d292f6e03661ae55a63686a0282ce65292087f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587341"
---
# New-AzureRmApiManagementRegion

## SYNOPSIS
Psapsananagementregion örneği oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Bir Psapsananagementregion örneği oluşturmak için yardımcı komutu.
Bu komut New-AzureRmApiManagement komutuyla kullanılır.

## ÖRNEKLERDEN

### Örnek 1
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### Örnek 2
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Orta ABD bölgesinde bir dış VpnType hizmeti Merkezi ABD 'de ek bir bölgeyle oluşturulur.

## PARAMETRELERINE

### -Kapasite
Azure API yönetim hizmeti ek bölgesinin SKU kapasitesi.
Varsayılan değer 1 ' dir.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.
Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırması.
Varsayılan değer $null.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. apsanana

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
