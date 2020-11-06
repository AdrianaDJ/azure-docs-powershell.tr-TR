---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: dcfa0968ac70f7a0abc14ee61ee615bee3aee5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592666"
---
# <span data-ttu-id="f8e06-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f8e06-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="f8e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e06-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e06-103">CDN özel etki alanını alır.</span><span class="sxs-lookup"><span data-stu-id="f8e06-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8e06-104">SYNTAX</span></span>

### <span data-ttu-id="f8e06-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8e06-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e06-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="f8e06-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e06-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8e06-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e06-108">**Get-AzureRmCdnCustomDomain** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) özel etki alanını ve ilgili ayarları alır.</span><span class="sxs-lookup"><span data-stu-id="f8e06-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="f8e06-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8e06-109">EXAMPLES</span></span>

## <span data-ttu-id="f8e06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8e06-110">PARAMETERS</span></span>

### <span data-ttu-id="f8e06-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8e06-111">-CdnEndpoint</span></span>
<span data-ttu-id="f8e06-112">Özel etki alanının üyesi olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e06-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="f8e06-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="f8e06-113">-CustomDomainName</span></span>
<span data-ttu-id="f8e06-114">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e06-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="f8e06-115">Özel etki alanının adı özel etki alanının ana bilgisayar adından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="f8e06-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f8e06-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f8e06-116">-EndpointName</span></span>
<span data-ttu-id="f8e06-117">Özel etki alanının ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e06-117">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f8e06-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f8e06-118">-ProfileName</span></span>
<span data-ttu-id="f8e06-119">Özel etki alanının ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e06-119">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f8e06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e06-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8e06-121">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e06-121">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f8e06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e06-122">-DefaultProfile</span></span>
<span data-ttu-id="f8e06-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8e06-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e06-124">CommonParameters</span></span>
<span data-ttu-id="f8e06-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8e06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e06-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e06-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8e06-127">INPUTS</span></span>

### <span data-ttu-id="f8e06-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8e06-128">PSEndpoint</span></span>
<span data-ttu-id="f8e06-129">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="f8e06-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f8e06-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8e06-130">OUTPUTS</span></span>

###  
<span data-ttu-id="f8e06-131">Bu cmdlet özel bir etki alanı nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f8e06-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="f8e06-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8e06-132">NOTES</span></span>

## <span data-ttu-id="f8e06-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8e06-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8e06-134">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f8e06-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="f8e06-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f8e06-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


