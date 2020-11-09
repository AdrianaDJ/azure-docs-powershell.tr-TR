---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325288"
---
# <span data-ttu-id="f4633-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="f4633-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="f4633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4633-102">SYNOPSIS</span></span>
<span data-ttu-id="f4633-103">ExpressRoutePort bağlantı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4633-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="f4633-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4633-104">SYNTAX</span></span>

### <span data-ttu-id="f4633-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4633-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4633-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f4633-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4633-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4633-107">DESCRIPTION</span></span>
<span data-ttu-id="f4633-108">**Get-AzExpressRoutePortLinkConfig** cmdlet 'ı ExpressRoutePort bağlantısının yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f4633-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="f4633-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4633-109">EXAMPLES</span></span>

### <span data-ttu-id="f4633-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4633-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="f4633-111">ExpressRoutePort 'un link1 yapılandırmasını alır $erport</span><span class="sxs-lookup"><span data-stu-id="f4633-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="f4633-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4633-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="f4633-113">ExpressRoutePort $erport RESOURCEID $id ile bağlantının yapılandırmasını alır</span><span class="sxs-lookup"><span data-stu-id="f4633-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="f4633-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4633-114">PARAMETERS</span></span>

### <span data-ttu-id="f4633-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4633-115">-DefaultProfile</span></span>
<span data-ttu-id="f4633-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4633-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4633-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f4633-117">-ExpressRoutePort</span></span>
<span data-ttu-id="f4633-118">ExpressRoutePort kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="f4633-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="f4633-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4633-119">-Name</span></span>
<span data-ttu-id="f4633-120">Bağlantının adı.</span><span class="sxs-lookup"><span data-stu-id="f4633-120">Name of the link.</span></span>

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

### <span data-ttu-id="f4633-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f4633-121">-ResourceId</span></span>
<span data-ttu-id="f4633-122">Bağlantının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="f4633-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="f4633-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4633-123">CommonParameters</span></span>
<span data-ttu-id="f4633-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4633-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4633-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4633-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4633-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4633-126">INPUTS</span></span>

### <span data-ttu-id="f4633-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f4633-127">System.String</span></span>

### <span data-ttu-id="f4633-128">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f4633-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f4633-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4633-129">OUTPUTS</span></span>

### <span data-ttu-id="f4633-130">Microsoft. Azure. Commands. Network. modeller. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="f4633-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="f4633-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4633-131">NOTES</span></span>

## <span data-ttu-id="f4633-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4633-132">RELATED LINKS</span></span>
