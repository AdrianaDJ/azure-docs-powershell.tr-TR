---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278842"
---
# <span data-ttu-id="b1150-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="b1150-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="b1150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1150-102">SYNOPSIS</span></span>
<span data-ttu-id="b1150-103">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="b1150-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b1150-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1150-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1150-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1150-105">DESCRIPTION</span></span>
<span data-ttu-id="b1150-106">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="b1150-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b1150-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1150-107">EXAMPLES</span></span>

### <span data-ttu-id="b1150-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1150-108">Example 1</span></span>
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

<span data-ttu-id="b1150-109">Desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin listesini döndürür:</span><span class="sxs-lookup"><span data-stu-id="b1150-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="b1150-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1150-110">PARAMETERS</span></span>

### <span data-ttu-id="b1150-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1150-111">-DefaultProfile</span></span>
<span data-ttu-id="b1150-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1150-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1150-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1150-113">-Name</span></span>
<span data-ttu-id="b1150-114">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="b1150-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="b1150-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1150-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1150-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b1150-116">The resource group name.</span></span>

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

### <span data-ttu-id="b1150-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1150-117">CommonParameters</span></span>
<span data-ttu-id="b1150-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1150-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1150-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1150-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1150-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1150-120">INPUTS</span></span>

### <span data-ttu-id="b1150-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b1150-121">System.String</span></span>

## <span data-ttu-id="b1150-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1150-122">OUTPUTS</span></span>

### <span data-ttu-id="b1150-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b1150-123">System.String</span></span>

## <span data-ttu-id="b1150-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1150-124">NOTES</span></span>

## <span data-ttu-id="b1150-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1150-125">RELATED LINKS</span></span>
