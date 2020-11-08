---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274156"
---
# <span data-ttu-id="268c6-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="268c6-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="268c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268c6-102">SYNOPSIS</span></span>
<span data-ttu-id="268c6-103">ExpressRoutePort 'a atanan kimliği alma.</span><span class="sxs-lookup"><span data-stu-id="268c6-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="268c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="268c6-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="268c6-105">DESCRIPTION</span></span>
<span data-ttu-id="268c6-106">**Get-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort nesnesine atanan kimliği alır.</span><span class="sxs-lookup"><span data-stu-id="268c6-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="268c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="268c6-107">EXAMPLES</span></span>

### <span data-ttu-id="268c6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="268c6-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="268c6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="268c6-109">PARAMETERS</span></span>

### <span data-ttu-id="268c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268c6-110">-DefaultProfile</span></span>
<span data-ttu-id="268c6-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="268c6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268c6-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="268c6-112">-ExpressRoutePort</span></span>
<span data-ttu-id="268c6-113">ExpressRoute bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="268c6-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="268c6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268c6-114">CommonParameters</span></span>
<span data-ttu-id="268c6-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="268c6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268c6-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="268c6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268c6-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="268c6-117">INPUTS</span></span>

### <span data-ttu-id="268c6-118">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="268c6-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="268c6-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="268c6-119">OUTPUTS</span></span>

### <span data-ttu-id="268c6-120">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="268c6-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="268c6-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="268c6-121">NOTES</span></span>

## <span data-ttu-id="268c6-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="268c6-122">RELATED LINKS</span></span>
[<span data-ttu-id="268c6-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="268c6-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="268c6-124">Yeni-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="268c6-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="268c6-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="268c6-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)