---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 5288ca32e43635db69598d72948e345f9e4c3256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932017"
---
# <span data-ttu-id="02088-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="02088-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="02088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02088-102">SYNOPSIS</span></span>
<span data-ttu-id="02088-103">ExpressRoutePort bağlantı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="02088-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="02088-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02088-104">SYNTAX</span></span>

### <span data-ttu-id="02088-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02088-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02088-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="02088-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02088-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="02088-107">DESCRIPTION</span></span>
<span data-ttu-id="02088-108">**Get-AzExpressRoutePortLinkConfig** cmdlet 'ı ExpressRoutePort bağlantısının yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="02088-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="02088-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02088-109">EXAMPLES</span></span>

### <span data-ttu-id="02088-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02088-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="02088-111">ExpressRoutePort 'un link1 yapılandırmasını alır $erport</span><span class="sxs-lookup"><span data-stu-id="02088-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="02088-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02088-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="02088-113">ExpressRoutePort $erport RESOURCEID $id ile bağlantının yapılandırmasını alır</span><span class="sxs-lookup"><span data-stu-id="02088-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="02088-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02088-114">PARAMETERS</span></span>

### <span data-ttu-id="02088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02088-115">-DefaultProfile</span></span>
<span data-ttu-id="02088-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02088-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02088-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="02088-117">-ExpressRoutePort</span></span>
<span data-ttu-id="02088-118">ExpressRoutePort kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="02088-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02088-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="02088-119">-Name</span></span>
<span data-ttu-id="02088-120">Bağlantının adı.</span><span class="sxs-lookup"><span data-stu-id="02088-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02088-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02088-121">-ResourceId</span></span>
<span data-ttu-id="02088-122">Bağlantının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="02088-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02088-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02088-123">CommonParameters</span></span>
<span data-ttu-id="02088-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02088-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02088-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02088-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02088-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02088-126">INPUTS</span></span>

### <span data-ttu-id="02088-127">System. String</span><span class="sxs-lookup"><span data-stu-id="02088-127">System.String</span></span>

### <span data-ttu-id="02088-128">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="02088-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="02088-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02088-129">OUTPUTS</span></span>

### <span data-ttu-id="02088-130">Microsoft. Azure. Commands. Network. modeller. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="02088-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="02088-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02088-131">NOTES</span></span>

## <span data-ttu-id="02088-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02088-132">RELATED LINKS</span></span>