---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097143"
---
# <span data-ttu-id="9b3a1-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="9b3a1-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="9b3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3a1-103">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="9b3a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b3a1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b3a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3a1-106">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="9b3a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b3a1-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3a1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b3a1-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="9b3a1-109">Desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin listesini döndürür:</span><span class="sxs-lookup"><span data-stu-id="9b3a1-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="9b3a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b3a1-110">PARAMETERS</span></span>

### <span data-ttu-id="9b3a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3a1-111">-DefaultProfile</span></span>
<span data-ttu-id="9b3a1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b3a1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b3a1-113">-Name</span></span>
<span data-ttu-id="9b3a1-114">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b3a1-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-116">The resource group name.</span></span>

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

### <span data-ttu-id="9b3a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3a1-117">CommonParameters</span></span>
<span data-ttu-id="9b3a1-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3a1-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3a1-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b3a1-120">INPUTS</span></span>

### <span data-ttu-id="9b3a1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9b3a1-121">System.String</span></span>

## <span data-ttu-id="9b3a1-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b3a1-122">OUTPUTS</span></span>

### <span data-ttu-id="9b3a1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9b3a1-123">System.String</span></span>

## <span data-ttu-id="9b3a1-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b3a1-124">NOTES</span></span>

## <span data-ttu-id="9b3a1-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b3a1-125">RELATED LINKS</span></span>