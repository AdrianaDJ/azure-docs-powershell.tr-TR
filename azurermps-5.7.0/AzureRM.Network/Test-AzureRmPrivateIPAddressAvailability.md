---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590389"
---
# <span data-ttu-id="f25f6-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="f25f6-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="f25f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f25f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f25f6-103">Sanal ağda özel bir IP adresinin uygunluğunu test edin.</span><span class="sxs-lookup"><span data-stu-id="f25f6-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f25f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f25f6-104">SYNTAX</span></span>

### <span data-ttu-id="f25f6-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="f25f6-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f25f6-106">Testbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f25f6-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f25f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f25f6-107">DESCRIPTION</span></span>
<span data-ttu-id="f25f6-108">**Test-AzureRmPrivateIPAddressAvailability** cmdlet 'i, belirli BIR özel IP adresinin sanal ağda kullanılabilir olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="f25f6-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="f25f6-109">Bu cmdlet, istenen özel IP adresi alındığında kullanılabilir özel IP adreslerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f25f6-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="f25f6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f25f6-110">EXAMPLES</span></span>

### <span data-ttu-id="f25f6-111">Örnek 1: ardışık düzeni kullanarak IP adresinin kullanılabilir olup olmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="f25f6-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="f25f6-112">Bu komut, sanal bir ağ alır ve belirtilen özel IP adresinin kullanılabilir olup olmadığını **Test** etmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f25f6-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="f25f6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f25f6-113">PARAMETERS</span></span>

### <span data-ttu-id="f25f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25f6-114">-DefaultProfile</span></span>
<span data-ttu-id="f25f6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f25f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f25f6-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f25f6-116">-IPAddress</span></span>
<span data-ttu-id="f25f6-117">Sınanacak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f25f6-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="f25f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f25f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="f25f6-119">Sanal ağ için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f25f6-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="f25f6-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f25f6-120">-VirtualNetwork</span></span>
<span data-ttu-id="f25f6-121">**PSVirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f25f6-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="f25f6-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f25f6-122">-VirtualNetworkName</span></span>
<span data-ttu-id="f25f6-123">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f25f6-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="f25f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25f6-124">CommonParameters</span></span>
<span data-ttu-id="f25f6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f25f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25f6-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f25f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25f6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f25f6-127">INPUTS</span></span>

### <span data-ttu-id="f25f6-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f25f6-128">PSVirtualNetwork</span></span>
<span data-ttu-id="f25f6-129">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f25f6-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="f25f6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f25f6-130">OUTPUTS</span></span>

### <span data-ttu-id="f25f6-131">Microsoft. Azure. Commands. Network. model. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="f25f6-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="f25f6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f25f6-132">NOTES</span></span>

## <span data-ttu-id="f25f6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f25f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="f25f6-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f25f6-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


