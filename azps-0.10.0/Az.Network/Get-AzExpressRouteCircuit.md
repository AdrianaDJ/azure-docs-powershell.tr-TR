---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935561"
---
# <span data-ttu-id="a0fe3-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a0fe3-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a0fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fe3-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="a0fe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0fe3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0fe3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fe3-106">**Get-Azexpressroutedevresi** cmdlet 'i aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="a0fe3-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="a0fe3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0fe3-108">EXAMPLES</span></span>

### <span data-ttu-id="a0fe3-109">Örnek 1: silinecek ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="a0fe3-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a0fe3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0fe3-110">PARAMETERS</span></span>

### <span data-ttu-id="a0fe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fe3-111">-DefaultProfile</span></span>
<span data-ttu-id="a0fe3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0fe3-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0fe3-113">-Name</span></span>
<span data-ttu-id="a0fe3-114">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a0fe3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fe3-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0fe3-116">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a0fe3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fe3-117">CommonParameters</span></span>
<span data-ttu-id="a0fe3-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0fe3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fe3-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0fe3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fe3-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0fe3-120">INPUTS</span></span>

## <span data-ttu-id="a0fe3-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0fe3-121">OUTPUTS</span></span>

### <span data-ttu-id="a0fe3-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a0fe3-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a0fe3-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0fe3-123">NOTES</span></span>

## <span data-ttu-id="a0fe3-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0fe3-124">RELATED LINKS</span></span>

[<span data-ttu-id="a0fe3-125">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a0fe3-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0fe3-126">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a0fe3-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0fe3-127">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a0fe3-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="a0fe3-128">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a0fe3-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
