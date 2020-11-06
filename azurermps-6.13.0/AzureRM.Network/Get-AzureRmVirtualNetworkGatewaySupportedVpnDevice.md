---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 97c832994e39707c0d45963eda856028589d4b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591943"
---
# <span data-ttu-id="02166-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="02166-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="02166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02166-102">SYNOPSIS</span></span>
<span data-ttu-id="02166-103">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="02166-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02166-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02166-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02166-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02166-105">DESCRIPTION</span></span>
<span data-ttu-id="02166-106">Bu Command, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="02166-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="02166-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02166-107">EXAMPLES</span></span>

### <span data-ttu-id="02166-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02166-108">Example 1</span></span>
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

<span data-ttu-id="02166-109">Desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin listesini döndürür:</span><span class="sxs-lookup"><span data-stu-id="02166-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="02166-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02166-110">PARAMETERS</span></span>

### <span data-ttu-id="02166-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02166-111">-DefaultProfile</span></span>
<span data-ttu-id="02166-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02166-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02166-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="02166-113">-Name</span></span>
<span data-ttu-id="02166-114">Sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="02166-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="02166-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02166-115">-ResourceGroupName</span></span>
<span data-ttu-id="02166-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02166-116">The resource group name.</span></span>

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

### <span data-ttu-id="02166-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02166-117">CommonParameters</span></span>
<span data-ttu-id="02166-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02166-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02166-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02166-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02166-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02166-120">INPUTS</span></span>

### <span data-ttu-id="02166-121">System. String</span><span class="sxs-lookup"><span data-stu-id="02166-121">System.String</span></span>

## <span data-ttu-id="02166-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02166-122">OUTPUTS</span></span>

### <span data-ttu-id="02166-123">System. String</span><span class="sxs-lookup"><span data-stu-id="02166-123">System.String</span></span>

## <span data-ttu-id="02166-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02166-124">NOTES</span></span>

## <span data-ttu-id="02166-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02166-125">RELATED LINKS</span></span>
