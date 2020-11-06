---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594379"
---
# <span data-ttu-id="43751-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="43751-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="43751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43751-102">SYNOPSIS</span></span>
<span data-ttu-id="43751-103">ExpressRoutePort bağlantı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="43751-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43751-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43751-104">SYNTAX</span></span>

### <span data-ttu-id="43751-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43751-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43751-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="43751-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43751-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="43751-107">DESCRIPTION</span></span>
<span data-ttu-id="43751-108">**Get-AzureRmExpressRoutePortLinkConfig** cmdlet 'ı ExpressRoutePort bağlantısının yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="43751-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="43751-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43751-109">EXAMPLES</span></span>

### <span data-ttu-id="43751-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="43751-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="43751-111">ExpressRoutePort 'un link1 yapılandırmasını alır $erport</span><span class="sxs-lookup"><span data-stu-id="43751-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="43751-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="43751-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="43751-113">ExpressRoutePort $erport RESOURCEID $id ile bağlantının yapılandırmasını alır</span><span class="sxs-lookup"><span data-stu-id="43751-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="43751-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43751-114">PARAMETERS</span></span>

### <span data-ttu-id="43751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43751-115">-DefaultProfile</span></span>
<span data-ttu-id="43751-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43751-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43751-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="43751-117">-ExpressRoutePort</span></span>
<span data-ttu-id="43751-118">ExpressRoutePort kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="43751-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="43751-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="43751-119">-Name</span></span>
<span data-ttu-id="43751-120">Bağlantının adı.</span><span class="sxs-lookup"><span data-stu-id="43751-120">Name of the link.</span></span>

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

### <span data-ttu-id="43751-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="43751-121">-ResourceId</span></span>
<span data-ttu-id="43751-122">Bağlantının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="43751-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="43751-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43751-123">CommonParameters</span></span>
<span data-ttu-id="43751-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43751-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43751-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43751-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43751-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43751-126">INPUTS</span></span>

### <span data-ttu-id="43751-127">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="43751-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="43751-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43751-128">OUTPUTS</span></span>

### <span data-ttu-id="43751-129">Microsoft. Azure. Commands. Network. modeller. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="43751-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="43751-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43751-130">NOTES</span></span>

## <span data-ttu-id="43751-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43751-131">RELATED LINKS</span></span>
