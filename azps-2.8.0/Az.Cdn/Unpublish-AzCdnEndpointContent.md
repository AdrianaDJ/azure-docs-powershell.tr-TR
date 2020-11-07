---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 6a5a0925967895514de8b7e5294c81571b1cbaba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753035"
---
# <span data-ttu-id="3a7f8-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3a7f8-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="3a7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7f8-103">CDN uç noktasını temizler.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="3a7f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a7f8-104">SYNTAX</span></span>

### <span data-ttu-id="3a7f8-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a7f8-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a7f8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7f8-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7f8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a7f8-107">DESCRIPTION</span></span>
<span data-ttu-id="3a7f8-108">**Yayımdan kaldırma-AzCdnEndpointContent** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasındaki içeriği temizler.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3a7f8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a7f8-109">EXAMPLES</span></span>

## <span data-ttu-id="3a7f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a7f8-110">PARAMETERS</span></span>

### <span data-ttu-id="3a7f8-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a7f8-111">-CdnEndpoint</span></span>
<span data-ttu-id="3a7f8-112">Bu cmdlet 'in temizler bitiş noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3a7f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7f8-113">-DefaultProfile</span></span>
<span data-ttu-id="3a7f8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3a7f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a7f8-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3a7f8-115">-EndpointName</span></span>
<span data-ttu-id="3a7f8-116">Bu cmdlet 'in temizler uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3a7f8-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a7f8-117">-PassThru</span></span>
<span data-ttu-id="3a7f8-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a7f8-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f8-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3a7f8-120">-ProfileName</span></span>
<span data-ttu-id="3a7f8-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3a7f8-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="3a7f8-122">-PurgeContent</span></span>
<span data-ttu-id="3a7f8-123">Bu cmdlet 'in temizler olduğu kaynak sunucuda içeriğin göreli yollarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a7f8-125">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3a7f8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a7f8-126">-Confirm</span></span>
<span data-ttu-id="3a7f8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7f8-128">-WhatIf</span></span>
<span data-ttu-id="3a7f8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a7f8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7f8-131">CommonParameters</span></span>
<span data-ttu-id="3a7f8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7f8-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a7f8-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7f8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a7f8-134">INPUTS</span></span>

### <span data-ttu-id="3a7f8-135">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a7f8-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="3a7f8-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a7f8-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a7f8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a7f8-137">OUTPUTS</span></span>

### <span data-ttu-id="3a7f8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a7f8-138">System.Boolean</span></span>

## <span data-ttu-id="3a7f8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a7f8-139">NOTES</span></span>

## <span data-ttu-id="3a7f8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a7f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a7f8-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3a7f8-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


