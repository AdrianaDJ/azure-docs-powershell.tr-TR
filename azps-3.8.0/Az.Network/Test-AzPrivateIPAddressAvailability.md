---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937676"
---
# <span data-ttu-id="6b200-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="6b200-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="6b200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b200-102">SYNOPSIS</span></span>
<span data-ttu-id="6b200-103">Sanal ağda özel bir IP adresinin uygunluğunu test edin.</span><span class="sxs-lookup"><span data-stu-id="6b200-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="6b200-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b200-104">SYNTAX</span></span>

### <span data-ttu-id="6b200-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="6b200-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b200-106">Testbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6b200-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b200-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b200-107">DESCRIPTION</span></span>
<span data-ttu-id="6b200-108">**Test-Azprivateıpaddressavailability** cmdlet 'i, belirli BIR özel IP adresinin sanal ağda kullanılabilir olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="6b200-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="6b200-109">Bu cmdlet, istenen özel IP adresi alındığında kullanılabilir özel IP adreslerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6b200-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="6b200-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b200-110">EXAMPLES</span></span>

### <span data-ttu-id="6b200-111">Örnek 1: ardışık düzeni kullanarak IP adresinin kullanılabilir olup olmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="6b200-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="6b200-112">Bu komut, sanal bir ağ alır ve belirtilen özel IP adresinin kullanılabilir olup olmadığını sınayan **-Azprivateıpaddressavailability** 'a geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6b200-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="6b200-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b200-113">PARAMETERS</span></span>

### <span data-ttu-id="6b200-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b200-114">-DefaultProfile</span></span>
<span data-ttu-id="6b200-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b200-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b200-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="6b200-116">-IPAddress</span></span>
<span data-ttu-id="6b200-117">Sınanacak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b200-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="6b200-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b200-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b200-119">Sanal ağ için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b200-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b200-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6b200-120">-VirtualNetwork</span></span>
<span data-ttu-id="6b200-121">**PSVirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b200-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b200-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6b200-122">-VirtualNetworkName</span></span>
<span data-ttu-id="6b200-123">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b200-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b200-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b200-124">CommonParameters</span></span>
<span data-ttu-id="6b200-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b200-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b200-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b200-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b200-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b200-127">INPUTS</span></span>

### <span data-ttu-id="6b200-128">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6b200-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6b200-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b200-129">OUTPUTS</span></span>

### <span data-ttu-id="6b200-130">Microsoft. Azure. Commands. Network. model. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="6b200-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="6b200-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b200-131">NOTES</span></span>

## <span data-ttu-id="6b200-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b200-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b200-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6b200-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


