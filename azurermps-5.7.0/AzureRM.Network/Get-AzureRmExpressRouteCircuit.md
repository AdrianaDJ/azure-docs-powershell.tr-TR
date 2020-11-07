---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763015"
---
# <span data-ttu-id="713cb-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="713cb-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="713cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="713cb-102">SYNOPSIS</span></span>
<span data-ttu-id="713cb-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="713cb-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="713cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="713cb-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="713cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="713cb-105">DESCRIPTION</span></span>
<span data-ttu-id="713cb-106">**Get-Azurermexpressroutedevresi** , aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="713cb-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="713cb-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="713cb-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="713cb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="713cb-108">EXAMPLES</span></span>

### <span data-ttu-id="713cb-109">Örnek 1: silinecek ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="713cb-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="713cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="713cb-110">PARAMETERS</span></span>

### <span data-ttu-id="713cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713cb-111">-DefaultProfile</span></span>
<span data-ttu-id="713cb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="713cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="713cb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="713cb-113">-Name</span></span>
<span data-ttu-id="713cb-114">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="713cb-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="713cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="713cb-116">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="713cb-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="713cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713cb-117">CommonParameters</span></span>
<span data-ttu-id="713cb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="713cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713cb-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="713cb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713cb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="713cb-120">INPUTS</span></span>

### <span data-ttu-id="713cb-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="713cb-121">None</span></span>
<span data-ttu-id="713cb-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="713cb-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="713cb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="713cb-123">OUTPUTS</span></span>

### <span data-ttu-id="713cb-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="713cb-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="713cb-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="713cb-125">NOTES</span></span>

## <span data-ttu-id="713cb-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="713cb-126">RELATED LINKS</span></span>

[<span data-ttu-id="713cb-127">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="713cb-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="713cb-128">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="713cb-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="713cb-129">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="713cb-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="713cb-130">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="713cb-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
