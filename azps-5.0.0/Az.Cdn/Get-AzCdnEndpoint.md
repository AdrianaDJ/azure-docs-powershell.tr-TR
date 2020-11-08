---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279541"
---
# <span data-ttu-id="c0cc0-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="c0cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cc0-103">CDN uç noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="c0cc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0cc0-104">SYNTAX</span></span>

### <span data-ttu-id="c0cc0-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0cc0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0cc0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cc0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0cc0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="c0cc0-108">**Get-Azcıdnendpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını ve ilişkili yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="c0cc0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0cc0-109">EXAMPLES</span></span>

## <span data-ttu-id="c0cc0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="c0cc0-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc0-111">-CdnProfile</span></span>
<span data-ttu-id="c0cc0-112">Uç noktanın ait olduğu CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c0cc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc0-113">-DefaultProfile</span></span>
<span data-ttu-id="c0cc0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0cc0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0cc0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c0cc0-115">-EndpointName</span></span>
<span data-ttu-id="c0cc0-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="c0cc0-117">Uç noktasının adı uç noktasının ana bilgisayar adı değildir.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="c0cc0-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c0cc0-118">-ProfileName</span></span>
<span data-ttu-id="c0cc0-119">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c0cc0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cc0-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0cc0-121">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c0cc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cc0-122">CommonParameters</span></span>
<span data-ttu-id="c0cc0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cc0-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0cc0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cc0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0cc0-125">INPUTS</span></span>

### <span data-ttu-id="c0cc0-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c0cc0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0cc0-127">OUTPUTS</span></span>

### <span data-ttu-id="c0cc0-128">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c0cc0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0cc0-129">NOTES</span></span>

## <span data-ttu-id="c0cc0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0cc0-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0cc0-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="c0cc0-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="c0cc0-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="c0cc0-134">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="c0cc0-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0cc0-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


