---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104909"
---
# <span data-ttu-id="7d6e4-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d6e4-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7d6e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6e4-103">CDN uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="7d6e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d6e4-104">SYNTAX</span></span>

### <span data-ttu-id="7d6e4-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d6e4-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6e4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d6e4-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d6e4-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6e4-108">**New-Azcıdncustomdomain** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7d6e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d6e4-109">EXAMPLES</span></span>

## <span data-ttu-id="7d6e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d6e4-110">PARAMETERS</span></span>

### <span data-ttu-id="7d6e4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d6e4-111">-CdnEndpoint</span></span>
<span data-ttu-id="7d6e4-112">Özel etki alanının eklendiği CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6e4-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="7d6e4-113">-CustomDomainName</span></span>
<span data-ttu-id="7d6e4-114">Özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6e4-115">-DefaultProfile</span></span>
<span data-ttu-id="7d6e4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7d6e4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d6e4-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7d6e4-117">-EndpointName</span></span>
<span data-ttu-id="7d6e4-118">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7d6e4-119">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="7d6e4-119">-HostName</span></span>
<span data-ttu-id="7d6e4-120">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6e4-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7d6e4-121">-ProfileName</span></span>
<span data-ttu-id="7d6e4-122">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7d6e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d6e4-124">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7d6e4-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d6e4-125">-Confirm</span></span>
<span data-ttu-id="7d6e4-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6e4-127">-WhatIf</span></span>
<span data-ttu-id="7d6e4-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6e4-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6e4-130">CommonParameters</span></span>
<span data-ttu-id="7d6e4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6e4-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d6e4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6e4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d6e4-133">INPUTS</span></span>

### <span data-ttu-id="7d6e4-134">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d6e4-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7d6e4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d6e4-135">OUTPUTS</span></span>

### <span data-ttu-id="7d6e4-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="7d6e4-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="7d6e4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d6e4-137">NOTES</span></span>

## <span data-ttu-id="7d6e4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d6e4-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d6e4-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d6e4-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7d6e4-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d6e4-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="7d6e4-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d6e4-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


