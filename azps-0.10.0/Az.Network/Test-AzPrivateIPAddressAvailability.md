---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 6a5ee3b03a4242c3c11d5c34da4a333ee7c82843
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936475"
---
# <span data-ttu-id="5e0b8-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="5e0b8-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="5e0b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0b8-103">Sanal ağda özel bir IP adresinin uygunluğunu test edin.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="5e0b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e0b8-104">SYNTAX</span></span>

### <span data-ttu-id="5e0b8-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="5e0b8-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e0b8-106">Testbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5e0b8-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e0b8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e0b8-107">DESCRIPTION</span></span>
<span data-ttu-id="5e0b8-108">**Test-Azprivateıpaddressavailability** cmdlet 'i, belirli BIR özel IP adresinin sanal ağda kullanılabilir olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="5e0b8-109">Bu cmdlet, istenen özel IP adresi alındığında kullanılabilir özel IP adreslerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="5e0b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e0b8-110">EXAMPLES</span></span>

### <span data-ttu-id="5e0b8-111">Örnek 1: ardışık düzeni kullanarak IP adresinin kullanılabilir olup olmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="5e0b8-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="5e0b8-112">Bu komut, sanal bir ağ alır ve belirtilen özel IP adresinin kullanılabilir olup olmadığını sınayan **-Azprivateıpaddressavailability** 'a geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="5e0b8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e0b8-113">PARAMETERS</span></span>

### <span data-ttu-id="5e0b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0b8-114">-DefaultProfile</span></span>
<span data-ttu-id="5e0b8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e0b8-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="5e0b8-116">-IPAddress</span></span>
<span data-ttu-id="5e0b8-117">Sınanacak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="5e0b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e0b8-119">Sanal ağ için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0b8-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e0b8-120">-VirtualNetwork</span></span>
<span data-ttu-id="5e0b8-121">**PSVirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0b8-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5e0b8-122">-VirtualNetworkName</span></span>
<span data-ttu-id="5e0b8-123">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0b8-124">CommonParameters</span></span>
<span data-ttu-id="5e0b8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e0b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0b8-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0b8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e0b8-127">INPUTS</span></span>

### <span data-ttu-id="5e0b8-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e0b8-128">PSVirtualNetwork</span></span>
<span data-ttu-id="5e0b8-129">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5e0b8-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5e0b8-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e0b8-130">OUTPUTS</span></span>

### <span data-ttu-id="5e0b8-131">Microsoft. Azure. Commands. Network. model. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="5e0b8-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="5e0b8-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e0b8-132">NOTES</span></span>

## <span data-ttu-id="5e0b8-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e0b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e0b8-134">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e0b8-134">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


