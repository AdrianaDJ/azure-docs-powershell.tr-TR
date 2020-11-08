---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098320"
---
# <span data-ttu-id="75419-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="75419-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="75419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75419-102">SYNOPSIS</span></span>
<span data-ttu-id="75419-103">İçeriği uç noktasına yükler.</span><span class="sxs-lookup"><span data-stu-id="75419-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="75419-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75419-104">SYNTAX</span></span>

### <span data-ttu-id="75419-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75419-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75419-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75419-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75419-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="75419-107">DESCRIPTION</span></span>
<span data-ttu-id="75419-108">**Publish-AzCdnEndpointContent** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktası için kaynak sunucudan içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="75419-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="75419-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75419-109">EXAMPLES</span></span>

## <span data-ttu-id="75419-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75419-110">PARAMETERS</span></span>

### <span data-ttu-id="75419-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="75419-111">-CdnEndpoint</span></span>
<span data-ttu-id="75419-112">CDN uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75419-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="75419-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75419-113">-DefaultProfile</span></span>
<span data-ttu-id="75419-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="75419-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75419-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="75419-115">-EndpointName</span></span>
<span data-ttu-id="75419-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75419-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="75419-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="75419-117">-LoadContent</span></span>
<span data-ttu-id="75419-118">Bu cmdlet 'in yayımladığı kaynak sunucuda içeriğin göreli yollarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75419-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="75419-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="75419-119">-PassThru</span></span>
<span data-ttu-id="75419-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="75419-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="75419-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="75419-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75419-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="75419-122">-ProfileName</span></span>
<span data-ttu-id="75419-123">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75419-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="75419-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75419-124">-ResourceGroupName</span></span>
<span data-ttu-id="75419-125">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75419-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="75419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75419-126">CommonParameters</span></span>
<span data-ttu-id="75419-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75419-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75419-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75419-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75419-129">INPUTS</span></span>

### <span data-ttu-id="75419-130">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="75419-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="75419-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75419-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75419-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75419-132">OUTPUTS</span></span>

### <span data-ttu-id="75419-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75419-133">System.Boolean</span></span>

## <span data-ttu-id="75419-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75419-134">NOTES</span></span>

## <span data-ttu-id="75419-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75419-135">RELATED LINKS</span></span>

[<span data-ttu-id="75419-136">Yayımdan kaldırma-Azcıcıendpointcontent</span><span class="sxs-lookup"><span data-stu-id="75419-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


