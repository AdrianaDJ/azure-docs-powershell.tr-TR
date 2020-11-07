---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: 3462e256889dffd086d9fa1d0fb96dba42ed109a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753092"
---
# <span data-ttu-id="144c2-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="144c2-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="144c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="144c2-102">SYNOPSIS</span></span>
<span data-ttu-id="144c2-103">CDN özel etki alanını alır.</span><span class="sxs-lookup"><span data-stu-id="144c2-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="144c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="144c2-104">SYNTAX</span></span>

### <span data-ttu-id="144c2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="144c2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="144c2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="144c2-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144c2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="144c2-107">DESCRIPTION</span></span>
<span data-ttu-id="144c2-108">**Get-AzCdnCustomDomain** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) özel etki alanını ve ilgili ayarları alır.</span><span class="sxs-lookup"><span data-stu-id="144c2-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="144c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="144c2-109">EXAMPLES</span></span>

## <span data-ttu-id="144c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="144c2-110">PARAMETERS</span></span>

### <span data-ttu-id="144c2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="144c2-111">-CdnEndpoint</span></span>
<span data-ttu-id="144c2-112">Özel etki alanının üyesi olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="144c2-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="144c2-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="144c2-113">-CustomDomainName</span></span>
<span data-ttu-id="144c2-114">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="144c2-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="144c2-115">Özel etki alanının adı özel etki alanının ana bilgisayar adından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="144c2-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="144c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144c2-116">-DefaultProfile</span></span>
<span data-ttu-id="144c2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="144c2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="144c2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="144c2-118">-EndpointName</span></span>
<span data-ttu-id="144c2-119">Özel etki alanının ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="144c2-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="144c2-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="144c2-120">-ProfileName</span></span>
<span data-ttu-id="144c2-121">Özel etki alanının ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="144c2-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="144c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="144c2-123">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="144c2-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="144c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144c2-124">CommonParameters</span></span>
<span data-ttu-id="144c2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="144c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144c2-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="144c2-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144c2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="144c2-127">INPUTS</span></span>

### <span data-ttu-id="144c2-128">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="144c2-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="144c2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="144c2-129">OUTPUTS</span></span>

### <span data-ttu-id="144c2-130">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="144c2-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="144c2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="144c2-131">NOTES</span></span>

## <span data-ttu-id="144c2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="144c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="144c2-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="144c2-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="144c2-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="144c2-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

