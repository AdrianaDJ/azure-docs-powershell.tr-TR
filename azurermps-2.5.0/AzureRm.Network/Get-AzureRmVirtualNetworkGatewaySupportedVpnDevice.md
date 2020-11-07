---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
ms.openlocfilehash: 46eccff9ad7b4fc525a864eab4c4477df4503dc2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939317"
---
# <span data-ttu-id="667c9-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="667c9-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="667c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667c9-102">SYNOPSIS</span></span>
<span data-ttu-id="667c9-103">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="667c9-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="667c9-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="667c9-105">DESCRIPTION</span></span>
<span data-ttu-id="667c9-106">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="667c9-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="667c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="667c9-107">EXAMPLES</span></span>

### <span data-ttu-id="667c9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="667c9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="667c9-109">Desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin listesini döndürür:</span><span class="sxs-lookup"><span data-stu-id="667c9-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="667c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="667c9-110">PARAMETERS</span></span>

### <span data-ttu-id="667c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667c9-111">-DefaultProfile</span></span>
<span data-ttu-id="667c9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="667c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667c9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="667c9-113">-Name</span></span>
<span data-ttu-id="667c9-114">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="667c9-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="667c9-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="667c9-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667c9-117">CommonParameters</span></span>
<span data-ttu-id="667c9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="667c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667c9-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667c9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667c9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="667c9-120">INPUTS</span></span>

### <span data-ttu-id="667c9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="667c9-121">System.String</span></span>

## <span data-ttu-id="667c9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="667c9-122">OUTPUTS</span></span>

### <span data-ttu-id="667c9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="667c9-123">System.String</span></span>

## <span data-ttu-id="667c9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="667c9-124">NOTES</span></span>

## <span data-ttu-id="667c9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="667c9-125">RELATED LINKS</span></span>

