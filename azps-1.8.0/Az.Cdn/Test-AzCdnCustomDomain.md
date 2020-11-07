---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 3ab4e9c673ebea17bbf15d4f978f7c500660060a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917547"
---
# <span data-ttu-id="b325f-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b325f-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="b325f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b325f-102">SYNOPSIS</span></span>
<span data-ttu-id="b325f-103">Özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="b325f-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="b325f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b325f-104">SYNTAX</span></span>

### <span data-ttu-id="b325f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b325f-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b325f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b325f-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b325f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b325f-107">DESCRIPTION</span></span>
<span data-ttu-id="b325f-108">**Test-Azcıdncustomdomain** cmdlet 'ı, CNAME eşlemesini doğrulayarak özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="b325f-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="b325f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b325f-109">EXAMPLES</span></span>

## <span data-ttu-id="b325f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b325f-110">PARAMETERS</span></span>

### <span data-ttu-id="b325f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b325f-111">-CdnEndpoint</span></span>
<span data-ttu-id="b325f-112">Özel etki alanını eklemek istediğiniz uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b325f-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="b325f-113">-Customdomainanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="b325f-113">-CustomDomainHostName</span></span>
<span data-ttu-id="b325f-114">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b325f-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="b325f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b325f-115">-DefaultProfile</span></span>
<span data-ttu-id="b325f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b325f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b325f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b325f-117">-EndpointName</span></span>
<span data-ttu-id="b325f-118">Özel etki alanını eklemek istediğiniz uç noktanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b325f-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="b325f-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b325f-119">-ProfileName</span></span>
<span data-ttu-id="b325f-120">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b325f-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b325f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b325f-121">-ResourceGroupName</span></span>
<span data-ttu-id="b325f-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b325f-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b325f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b325f-123">CommonParameters</span></span>
<span data-ttu-id="b325f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b325f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b325f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b325f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b325f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b325f-126">INPUTS</span></span>

### <span data-ttu-id="b325f-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b325f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b325f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b325f-128">OUTPUTS</span></span>

### <span data-ttu-id="b325f-129">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="b325f-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="b325f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b325f-130">NOTES</span></span>

## <span data-ttu-id="b325f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b325f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b325f-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b325f-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="b325f-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b325f-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="b325f-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b325f-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


