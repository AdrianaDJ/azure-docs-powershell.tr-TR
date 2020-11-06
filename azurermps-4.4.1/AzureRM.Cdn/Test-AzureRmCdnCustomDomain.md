---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591125"
---
# <span data-ttu-id="a08cd-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a08cd-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a08cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a08cd-103">Özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="a08cd-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a08cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a08cd-104">SYNTAX</span></span>

### <span data-ttu-id="a08cd-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a08cd-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08cd-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="a08cd-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a08cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a08cd-107">DESCRIPTION</span></span>
<span data-ttu-id="a08cd-108">**Test-AzureRmCdnCustomDomain** cmdlet 'ı, CNAME eşlemesini doğrulayarak özel bir etki alanının uç noktasına eklenip eklenemeyeceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="a08cd-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="a08cd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a08cd-109">EXAMPLES</span></span>

## <span data-ttu-id="a08cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a08cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a08cd-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a08cd-111">-CdnEndpoint</span></span>
<span data-ttu-id="a08cd-112">Özel etki alanını eklemek istediğiniz uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08cd-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="a08cd-113">-Customdomainanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="a08cd-113">-CustomDomainHostName</span></span>
<span data-ttu-id="a08cd-114">Özel etki alanının ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08cd-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="a08cd-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a08cd-115">-EndpointName</span></span>
<span data-ttu-id="a08cd-116">Özel etki alanını eklemek istediğiniz uç noktanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08cd-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="a08cd-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a08cd-117">-ProfileName</span></span>
<span data-ttu-id="a08cd-118">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08cd-118">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a08cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="a08cd-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a08cd-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a08cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08cd-121">-DefaultProfile</span></span>
<span data-ttu-id="a08cd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a08cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a08cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08cd-123">CommonParameters</span></span>
<span data-ttu-id="a08cd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a08cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08cd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a08cd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08cd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a08cd-126">INPUTS</span></span>

### <span data-ttu-id="a08cd-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a08cd-127">PSEndpoint</span></span>
<span data-ttu-id="a08cd-128">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="a08cd-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a08cd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a08cd-129">OUTPUTS</span></span>

### <span data-ttu-id="a08cd-130">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="a08cd-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="a08cd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a08cd-131">NOTES</span></span>

## <span data-ttu-id="a08cd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a08cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="a08cd-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a08cd-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a08cd-134">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a08cd-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a08cd-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a08cd-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


