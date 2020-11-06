---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2788c135f7c93d0ca2f3a8dbb17228e4118625c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587649"
---
# <span data-ttu-id="8e298-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="8e298-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="8e298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e298-102">SYNOPSIS</span></span>
<span data-ttu-id="8e298-103">CDN uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e298-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e298-104">SYNTAX</span></span>

### <span data-ttu-id="8e298-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e298-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e298-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e298-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e298-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e298-107">DESCRIPTION</span></span>
<span data-ttu-id="8e298-108">**New-AzureRmCdnCustomDomain** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktası için özel bir etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e298-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8e298-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e298-109">EXAMPLES</span></span>

## <span data-ttu-id="8e298-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e298-110">PARAMETERS</span></span>

### <span data-ttu-id="8e298-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e298-111">-CdnEndpoint</span></span>
<span data-ttu-id="8e298-112">Özel etki alanının eklendiği CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="8e298-113">-CustomDomainName</span></span>
<span data-ttu-id="8e298-114">Özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e298-115">-DefaultProfile</span></span>
<span data-ttu-id="8e298-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8e298-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8e298-117">-EndpointName</span></span>
<span data-ttu-id="8e298-118">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-119">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="8e298-119">-HostName</span></span>
<span data-ttu-id="8e298-120">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8e298-121">-ProfileName</span></span>
<span data-ttu-id="8e298-122">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-122">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e298-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e298-124">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e298-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e298-125">-Confirm</span></span>
<span data-ttu-id="8e298-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e298-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e298-127">-WhatIf</span></span>
<span data-ttu-id="8e298-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e298-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e298-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e298-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e298-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e298-130">CommonParameters</span></span>
<span data-ttu-id="8e298-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e298-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e298-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e298-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e298-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e298-133">INPUTS</span></span>

### <span data-ttu-id="8e298-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e298-134">PSEndpoint</span></span>
<span data-ttu-id="8e298-135">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8e298-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="8e298-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e298-136">OUTPUTS</span></span>

### <span data-ttu-id="8e298-137">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="8e298-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="8e298-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e298-138">NOTES</span></span>

## <span data-ttu-id="8e298-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e298-139">RELATED LINKS</span></span>

[<span data-ttu-id="8e298-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="8e298-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="8e298-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="8e298-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="8e298-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="8e298-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


