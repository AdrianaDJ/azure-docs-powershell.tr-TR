---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763403"
---
# <span data-ttu-id="e6dd2-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6dd2-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="e6dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e6dd2-103">CDN uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6dd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6dd2-104">SYNTAX</span></span>

### <span data-ttu-id="e6dd2-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6dd2-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6dd2-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="e6dd2-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6dd2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6dd2-107">DESCRIPTION</span></span>
<span data-ttu-id="e6dd2-108">**New-AzureRmCdnCustomDomain** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e6dd2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6dd2-109">EXAMPLES</span></span>

## <span data-ttu-id="e6dd2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6dd2-110">PARAMETERS</span></span>

### <span data-ttu-id="e6dd2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6dd2-111">-CdnEndpoint</span></span>
<span data-ttu-id="e6dd2-112">Özel etki alanının eklendiği CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="e6dd2-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="e6dd2-113">-CustomDomainName</span></span>
<span data-ttu-id="e6dd2-114">Özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="e6dd2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e6dd2-115">-EndpointName</span></span>
<span data-ttu-id="e6dd2-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e6dd2-117">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="e6dd2-117">-HostName</span></span>
<span data-ttu-id="e6dd2-118">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-118">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="e6dd2-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e6dd2-119">-ProfileName</span></span>
<span data-ttu-id="e6dd2-120">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e6dd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6dd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6dd2-122">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="e6dd2-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6dd2-123">-Confirm</span></span>
<span data-ttu-id="e6dd2-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6dd2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6dd2-125">-WhatIf</span></span>
<span data-ttu-id="e6dd2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6dd2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6dd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6dd2-128">-DefaultProfile</span></span>
<span data-ttu-id="e6dd2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6dd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6dd2-130">CommonParameters</span></span>
<span data-ttu-id="e6dd2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6dd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6dd2-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6dd2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6dd2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6dd2-133">INPUTS</span></span>

### <span data-ttu-id="e6dd2-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6dd2-134">PSEndpoint</span></span>
<span data-ttu-id="e6dd2-135">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="e6dd2-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e6dd2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6dd2-136">OUTPUTS</span></span>

### <span data-ttu-id="e6dd2-137">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="e6dd2-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="e6dd2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6dd2-138">NOTES</span></span>

## <span data-ttu-id="e6dd2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6dd2-139">RELATED LINKS</span></span>

[<span data-ttu-id="e6dd2-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6dd2-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e6dd2-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6dd2-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e6dd2-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6dd2-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


