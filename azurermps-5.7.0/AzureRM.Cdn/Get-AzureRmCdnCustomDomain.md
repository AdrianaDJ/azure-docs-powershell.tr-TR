---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587662"
---
# <span data-ttu-id="72663-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="72663-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="72663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72663-102">SYNOPSIS</span></span>
<span data-ttu-id="72663-103">CDN özel etki alanını alır.</span><span class="sxs-lookup"><span data-stu-id="72663-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72663-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72663-104">SYNTAX</span></span>

### <span data-ttu-id="72663-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72663-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72663-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72663-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72663-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72663-107">DESCRIPTION</span></span>
<span data-ttu-id="72663-108">**Get-AzureRmCdnCustomDomain** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) özel etki alanını ve ilgili ayarları alır.</span><span class="sxs-lookup"><span data-stu-id="72663-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="72663-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72663-109">EXAMPLES</span></span>

## <span data-ttu-id="72663-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72663-110">PARAMETERS</span></span>

### <span data-ttu-id="72663-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72663-111">-CdnEndpoint</span></span>
<span data-ttu-id="72663-112">Özel etki alanının üyesi olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72663-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="72663-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="72663-113">-CustomDomainName</span></span>
<span data-ttu-id="72663-114">Özel etki alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72663-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="72663-115">Özel etki alanının adı özel etki alanının ana bilgisayar adından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="72663-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72663-116">-DefaultProfile</span></span>
<span data-ttu-id="72663-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72663-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72663-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="72663-118">-EndpointName</span></span>
<span data-ttu-id="72663-119">Özel etki alanının ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72663-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="72663-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="72663-120">-ProfileName</span></span>
<span data-ttu-id="72663-121">Özel etki alanının ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72663-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="72663-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72663-122">-ResourceGroupName</span></span>
<span data-ttu-id="72663-123">Özel etki alanının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72663-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="72663-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72663-124">CommonParameters</span></span>
<span data-ttu-id="72663-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72663-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72663-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72663-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72663-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72663-127">INPUTS</span></span>

### <span data-ttu-id="72663-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="72663-128">PSEndpoint</span></span>
<span data-ttu-id="72663-129">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="72663-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="72663-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72663-130">OUTPUTS</span></span>

###  
<span data-ttu-id="72663-131">Bu cmdlet özel bir etki alanı nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="72663-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="72663-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72663-132">NOTES</span></span>

## <span data-ttu-id="72663-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72663-133">RELATED LINKS</span></span>

[<span data-ttu-id="72663-134">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="72663-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="72663-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="72663-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


