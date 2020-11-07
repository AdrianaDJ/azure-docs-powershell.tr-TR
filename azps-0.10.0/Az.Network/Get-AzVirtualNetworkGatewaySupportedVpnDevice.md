---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935466"
---
# <span data-ttu-id="f4fe3-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="f4fe3-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="f4fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fe3-103">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f4fe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4fe3-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4fe3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="f4fe3-106">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f4fe3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4fe3-107">EXAMPLES</span></span>

### <span data-ttu-id="f4fe3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4fe3-108">Example 1</span></span>
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

<span data-ttu-id="f4fe3-109">Desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin listesini döndürür:</span><span class="sxs-lookup"><span data-stu-id="f4fe3-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="f4fe3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4fe3-110">PARAMETERS</span></span>

### <span data-ttu-id="f4fe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fe3-111">-DefaultProfile</span></span>
<span data-ttu-id="f4fe3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fe3-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4fe3-113">-Name</span></span>
<span data-ttu-id="f4fe3-114">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="f4fe3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fe3-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4fe3-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-116">The resource group name.</span></span>

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

### <span data-ttu-id="f4fe3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fe3-117">CommonParameters</span></span>
<span data-ttu-id="f4fe3-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4fe3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fe3-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fe3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fe3-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4fe3-120">INPUTS</span></span>

### <span data-ttu-id="f4fe3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fe3-121">System.String</span></span>

## <span data-ttu-id="f4fe3-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4fe3-122">OUTPUTS</span></span>

### <span data-ttu-id="f4fe3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fe3-123">System.String</span></span>

## <span data-ttu-id="f4fe3-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4fe3-124">NOTES</span></span>

## <span data-ttu-id="f4fe3-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4fe3-125">RELATED LINKS</span></span>

