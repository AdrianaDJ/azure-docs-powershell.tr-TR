---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: eb4215a281b83bd533a7502e3ec538ec4e3a570c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592332"
---
# <span data-ttu-id="8d1f2-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="8d1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1f2-103">CDN uç noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d1f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d1f2-104">SYNTAX</span></span>

### <span data-ttu-id="8d1f2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d1f2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d1f2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d1f2-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1f2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d1f2-107">DESCRIPTION</span></span>
<span data-ttu-id="8d1f2-108">**Get-AzureRMCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını ve ilişkili yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="8d1f2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d1f2-109">EXAMPLES</span></span>

## <span data-ttu-id="8d1f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d1f2-110">PARAMETERS</span></span>

### <span data-ttu-id="8d1f2-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8d1f2-111">-CdnProfile</span></span>
<span data-ttu-id="8d1f2-112">Uç noktanın ait olduğu CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8d1f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1f2-113">-DefaultProfile</span></span>
<span data-ttu-id="8d1f2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8d1f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d1f2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8d1f2-115">-EndpointName</span></span>
<span data-ttu-id="8d1f2-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="8d1f2-117">Uç noktasının adı uç noktasının ana bilgisayar adı değildir.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="8d1f2-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8d1f2-118">-ProfileName</span></span>
<span data-ttu-id="8d1f2-119">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8d1f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d1f2-121">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="8d1f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1f2-122">CommonParameters</span></span>
<span data-ttu-id="8d1f2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d1f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1f2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1f2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d1f2-125">INPUTS</span></span>

### <span data-ttu-id="8d1f2-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="8d1f2-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="8d1f2-127">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d1f2-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="8d1f2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d1f2-128">OUTPUTS</span></span>

### <span data-ttu-id="8d1f2-129">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8d1f2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d1f2-130">NOTES</span></span>

## <span data-ttu-id="8d1f2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d1f2-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d1f2-132">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8d1f2-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8d1f2-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8d1f2-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="8d1f2-136">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d1f2-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


