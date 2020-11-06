---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591392"
---
# <span data-ttu-id="7707c-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="7707c-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="7707c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7707c-102">SYNOPSIS</span></span>
<span data-ttu-id="7707c-103">İçeriği uç noktasına yükler.</span><span class="sxs-lookup"><span data-stu-id="7707c-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7707c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7707c-104">SYNTAX</span></span>

### <span data-ttu-id="7707c-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7707c-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7707c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7707c-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7707c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7707c-107">DESCRIPTION</span></span>
<span data-ttu-id="7707c-108">**Publish-AzureRmCdnEndpointContent** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktası için kaynak sunucudan içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="7707c-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7707c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7707c-109">EXAMPLES</span></span>

## <span data-ttu-id="7707c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7707c-110">PARAMETERS</span></span>

### <span data-ttu-id="7707c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7707c-111">-CdnEndpoint</span></span>
<span data-ttu-id="7707c-112">CDN uç noktasını büyütür.</span><span class="sxs-lookup"><span data-stu-id="7707c-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="7707c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7707c-113">-DefaultProfile</span></span>
<span data-ttu-id="7707c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7707c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7707c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7707c-115">-EndpointName</span></span>
<span data-ttu-id="7707c-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7707c-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7707c-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="7707c-117">-LoadContent</span></span>
<span data-ttu-id="7707c-118">Bu cmdlet 'in yayımladığı kaynak sunucuda içeriğin göreli yollarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7707c-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="7707c-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7707c-119">-PassThru</span></span>
<span data-ttu-id="7707c-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7707c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7707c-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7707c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7707c-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7707c-122">-ProfileName</span></span>
<span data-ttu-id="7707c-123">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7707c-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="7707c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7707c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7707c-125">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7707c-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="7707c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7707c-126">CommonParameters</span></span>
<span data-ttu-id="7707c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7707c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7707c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7707c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7707c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7707c-129">INPUTS</span></span>

### <span data-ttu-id="7707c-130">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7707c-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="7707c-131">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7707c-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="7707c-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7707c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7707c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7707c-133">OUTPUTS</span></span>

### <span data-ttu-id="7707c-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7707c-134">System.Boolean</span></span>

## <span data-ttu-id="7707c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7707c-135">NOTES</span></span>

## <span data-ttu-id="7707c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7707c-136">RELATED LINKS</span></span>

[<span data-ttu-id="7707c-137">Yayımdan kaldırma-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="7707c-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


