---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097672"
---
# <span data-ttu-id="0ff4e-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="0ff4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff4e-103">CDN uç noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="0ff4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ff4e-104">SYNTAX</span></span>

### <span data-ttu-id="0ff4e-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ff4e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ff4e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ff4e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ff4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ff4e-107">DESCRIPTION</span></span>
<span data-ttu-id="0ff4e-108">**Get-Azcıdnendpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını ve ilişkili yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="0ff4e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ff4e-109">EXAMPLES</span></span>

## <span data-ttu-id="0ff4e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ff4e-110">PARAMETERS</span></span>

### <span data-ttu-id="0ff4e-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0ff4e-111">-CdnProfile</span></span>
<span data-ttu-id="0ff4e-112">Uç noktanın ait olduğu CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff4e-113">-DefaultProfile</span></span>
<span data-ttu-id="0ff4e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0ff4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ff4e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0ff4e-115">-EndpointName</span></span>
<span data-ttu-id="0ff4e-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="0ff4e-117">Uç noktasının adı uç noktasının ana bilgisayar adı değildir.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff4e-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0ff4e-118">-ProfileName</span></span>
<span data-ttu-id="0ff4e-119">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff4e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff4e-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ff4e-121">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff4e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff4e-122">CommonParameters</span></span>
<span data-ttu-id="0ff4e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff4e-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ff4e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff4e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ff4e-125">INPUTS</span></span>

### <span data-ttu-id="0ff4e-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0ff4e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="0ff4e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ff4e-127">OUTPUTS</span></span>

### <span data-ttu-id="0ff4e-128">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0ff4e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ff4e-129">NOTES</span></span>

## <span data-ttu-id="0ff4e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ff4e-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ff4e-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="0ff4e-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="0ff4e-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="0ff4e-134">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="0ff4e-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ff4e-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


