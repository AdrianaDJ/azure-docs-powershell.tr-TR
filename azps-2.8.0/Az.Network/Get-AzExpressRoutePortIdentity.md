---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: f8b41145c29d0eb3b2485fb1eb6b969574686b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931757"
---
# <span data-ttu-id="5097d-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5097d-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="5097d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5097d-102">SYNOPSIS</span></span>
<span data-ttu-id="5097d-103">ExpressRoutePort 'a atanan kimliği alma.</span><span class="sxs-lookup"><span data-stu-id="5097d-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="5097d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5097d-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5097d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5097d-105">DESCRIPTION</span></span>
<span data-ttu-id="5097d-106">**Get-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort nesnesine atanan kimliği alır.</span><span class="sxs-lookup"><span data-stu-id="5097d-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="5097d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5097d-107">EXAMPLES</span></span>

### <span data-ttu-id="5097d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5097d-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="5097d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5097d-109">PARAMETERS</span></span>

### <span data-ttu-id="5097d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5097d-110">-DefaultProfile</span></span>
<span data-ttu-id="5097d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5097d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5097d-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5097d-112">-ExpressRoutePort</span></span>
<span data-ttu-id="5097d-113">ExpressRoute bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="5097d-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5097d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5097d-114">CommonParameters</span></span>
<span data-ttu-id="5097d-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5097d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5097d-116">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5097d-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5097d-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5097d-117">INPUTS</span></span>

### <span data-ttu-id="5097d-118">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="5097d-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="5097d-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5097d-119">OUTPUTS</span></span>

### <span data-ttu-id="5097d-120">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="5097d-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="5097d-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5097d-121">NOTES</span></span>

## <span data-ttu-id="5097d-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5097d-122">RELATED LINKS</span></span>
[<span data-ttu-id="5097d-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5097d-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5097d-124">Yeni-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5097d-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="5097d-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="5097d-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)