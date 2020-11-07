---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 15ab6c6974924458e6a206dac3d3629f3f4c48a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763469"
---
# <span data-ttu-id="1dcc5-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="1dcc5-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="1dcc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcc5-103">CDN uç noktasını temizler.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dcc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dcc5-104">SYNTAX</span></span>

### <span data-ttu-id="1dcc5-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1dcc5-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dcc5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dcc5-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dcc5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dcc5-107">DESCRIPTION</span></span>
<span data-ttu-id="1dcc5-108">**Yayımdan kaldırma-AzureRmCdnEndpointContent** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasındaki içeriği temizler.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1dcc5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dcc5-109">EXAMPLES</span></span>

## <span data-ttu-id="1dcc5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dcc5-110">PARAMETERS</span></span>

### <span data-ttu-id="1dcc5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1dcc5-111">-CdnEndpoint</span></span>
<span data-ttu-id="1dcc5-112">Bu cmdlet 'in temizler bitiş noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="1dcc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcc5-113">-DefaultProfile</span></span>
<span data-ttu-id="1dcc5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1dcc5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dcc5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1dcc5-115">-EndpointName</span></span>
<span data-ttu-id="1dcc5-116">Bu cmdlet 'in temizler uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="1dcc5-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1dcc5-117">-PassThru</span></span>
<span data-ttu-id="1dcc5-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1dcc5-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1dcc5-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1dcc5-120">-ProfileName</span></span>
<span data-ttu-id="1dcc5-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="1dcc5-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="1dcc5-122">-PurgeContent</span></span>
<span data-ttu-id="1dcc5-123">Bu cmdlet 'in temizler olduğu kaynak sunucuda içeriğin göreli yollarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="1dcc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dcc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dcc5-125">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="1dcc5-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1dcc5-126">-Confirm</span></span>
<span data-ttu-id="1dcc5-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dcc5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dcc5-128">-WhatIf</span></span>
<span data-ttu-id="1dcc5-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dcc5-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dcc5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcc5-131">CommonParameters</span></span>
<span data-ttu-id="1dcc5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dcc5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcc5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dcc5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcc5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dcc5-134">INPUTS</span></span>

### <span data-ttu-id="1dcc5-135">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1dcc5-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="1dcc5-136">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1dcc5-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="1dcc5-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1dcc5-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1dcc5-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dcc5-138">OUTPUTS</span></span>

### <span data-ttu-id="1dcc5-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dcc5-139">System.Boolean</span></span>

## <span data-ttu-id="1dcc5-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dcc5-140">NOTES</span></span>

## <span data-ttu-id="1dcc5-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dcc5-141">RELATED LINKS</span></span>

[<span data-ttu-id="1dcc5-142">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="1dcc5-142">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)

