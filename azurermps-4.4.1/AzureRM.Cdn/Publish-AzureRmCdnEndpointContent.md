---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592653"
---
# <span data-ttu-id="272c6-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="272c6-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="272c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272c6-102">SYNOPSIS</span></span>
<span data-ttu-id="272c6-103">İçeriği uç noktasına yükler.</span><span class="sxs-lookup"><span data-stu-id="272c6-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="272c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="272c6-104">SYNTAX</span></span>

### <span data-ttu-id="272c6-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="272c6-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272c6-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="272c6-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="272c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="272c6-107">DESCRIPTION</span></span>
<span data-ttu-id="272c6-108">**Publish-AzureRmCdnEndpointContent** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktası için kaynak sunucudan içerik yükler.</span><span class="sxs-lookup"><span data-stu-id="272c6-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="272c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="272c6-109">EXAMPLES</span></span>

## <span data-ttu-id="272c6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="272c6-110">PARAMETERS</span></span>

### <span data-ttu-id="272c6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="272c6-111">-CdnEndpoint</span></span>
<span data-ttu-id="272c6-112">CDN uç noktasını büyütür.</span><span class="sxs-lookup"><span data-stu-id="272c6-112">Sepcifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="272c6-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="272c6-113">-EndpointName</span></span>
<span data-ttu-id="272c6-114">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="272c6-114">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272c6-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="272c6-115">-LoadContent</span></span>
<span data-ttu-id="272c6-116">Bu cmdlet 'in yayımladığı kaynak sunucuda içeriğin göreli yollarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="272c6-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="272c6-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="272c6-117">-PassThru</span></span>
<span data-ttu-id="272c6-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="272c6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="272c6-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="272c6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="272c6-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="272c6-120">-ProfileName</span></span>
<span data-ttu-id="272c6-121">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="272c6-121">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="272c6-123">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="272c6-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272c6-124">-DefaultProfile</span></span>
<span data-ttu-id="272c6-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="272c6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="272c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272c6-126">CommonParameters</span></span>
<span data-ttu-id="272c6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="272c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272c6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272c6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="272c6-129">INPUTS</span></span>

### <span data-ttu-id="272c6-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="272c6-130">PSEndpoint</span></span>
<span data-ttu-id="272c6-131">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="272c6-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="272c6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="272c6-132">OUTPUTS</span></span>

### <span data-ttu-id="272c6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="272c6-133">System.Boolean</span></span>

## <span data-ttu-id="272c6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="272c6-134">NOTES</span></span>

## <span data-ttu-id="272c6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="272c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="272c6-136">Yayımdan kaldırma-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="272c6-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


