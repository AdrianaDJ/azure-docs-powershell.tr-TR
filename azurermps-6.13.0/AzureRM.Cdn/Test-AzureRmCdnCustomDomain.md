---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592791"
---
# <span data-ttu-id="107a2-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="107a2-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="107a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107a2-102">SYNOPSIS</span></span>
<span data-ttu-id="107a2-103">Özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="107a2-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="107a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="107a2-104">SYNTAX</span></span>

### <span data-ttu-id="107a2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="107a2-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="107a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="107a2-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="107a2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="107a2-107">DESCRIPTION</span></span>
<span data-ttu-id="107a2-108">**Test-AzureRmCdnCustomDomain** cmdlet 'ı, CNAME eşlemesini doğrulayarak özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="107a2-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="107a2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="107a2-109">EXAMPLES</span></span>

## <span data-ttu-id="107a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="107a2-110">PARAMETERS</span></span>

### <span data-ttu-id="107a2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="107a2-111">-CdnEndpoint</span></span>
<span data-ttu-id="107a2-112">Özel etki alanını eklemek istediğiniz uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a2-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="107a2-113">-Customdomainanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="107a2-113">-CustomDomainHostName</span></span>
<span data-ttu-id="107a2-114">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a2-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="107a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107a2-115">-DefaultProfile</span></span>
<span data-ttu-id="107a2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="107a2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107a2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="107a2-117">-EndpointName</span></span>
<span data-ttu-id="107a2-118">Özel etki alanını eklemek istediğiniz uç noktanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a2-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="107a2-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="107a2-119">-ProfileName</span></span>
<span data-ttu-id="107a2-120">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a2-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="107a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="107a2-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a2-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="107a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107a2-123">CommonParameters</span></span>
<span data-ttu-id="107a2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="107a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107a2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107a2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107a2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="107a2-126">INPUTS</span></span>

### <span data-ttu-id="107a2-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="107a2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="107a2-128">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="107a2-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="107a2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="107a2-129">OUTPUTS</span></span>

### <span data-ttu-id="107a2-130">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="107a2-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="107a2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="107a2-131">NOTES</span></span>

## <span data-ttu-id="107a2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="107a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="107a2-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="107a2-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="107a2-134">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="107a2-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="107a2-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="107a2-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


