---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279210"
---
# <span data-ttu-id="fe8f2-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fe8f2-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="fe8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8f2-103">Özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="fe8f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe8f2-104">SYNTAX</span></span>

### <span data-ttu-id="fe8f2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe8f2-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe8f2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8f2-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe8f2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe8f2-107">DESCRIPTION</span></span>
<span data-ttu-id="fe8f2-108">**Test-Azcıdncustomdomain** cmdlet 'ı, CNAME eşlemesini doğrulayarak özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="fe8f2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe8f2-109">EXAMPLES</span></span>

## <span data-ttu-id="fe8f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe8f2-110">PARAMETERS</span></span>

### <span data-ttu-id="fe8f2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe8f2-111">-CdnEndpoint</span></span>
<span data-ttu-id="fe8f2-112">Özel etki alanını eklemek istediğiniz uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fe8f2-113">-Customdomainanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="fe8f2-113">-CustomDomainHostName</span></span>
<span data-ttu-id="fe8f2-114">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="fe8f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8f2-115">-DefaultProfile</span></span>
<span data-ttu-id="fe8f2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fe8f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe8f2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fe8f2-117">-EndpointName</span></span>
<span data-ttu-id="fe8f2-118">Özel etki alanını eklemek istediğiniz uç noktanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fe8f2-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fe8f2-119">-ProfileName</span></span>
<span data-ttu-id="fe8f2-120">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fe8f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe8f2-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fe8f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8f2-123">CommonParameters</span></span>
<span data-ttu-id="fe8f2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8f2-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe8f2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8f2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe8f2-126">INPUTS</span></span>

### <span data-ttu-id="fe8f2-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe8f2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fe8f2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe8f2-128">OUTPUTS</span></span>

### <span data-ttu-id="fe8f2-129">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="fe8f2-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="fe8f2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe8f2-130">NOTES</span></span>

## <span data-ttu-id="fe8f2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe8f2-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe8f2-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fe8f2-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="fe8f2-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fe8f2-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="fe8f2-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fe8f2-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


