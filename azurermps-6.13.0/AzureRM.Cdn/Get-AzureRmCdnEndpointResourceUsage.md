---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590963"
---
# <span data-ttu-id="3b1ec-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3b1ec-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="3b1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1ec-103">CDN uç noktasının kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b1ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b1ec-104">SYNTAX</span></span>

### <span data-ttu-id="3b1ec-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b1ec-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b1ec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1ec-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b1ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b1ec-107">DESCRIPTION</span></span>
<span data-ttu-id="3b1ec-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="3b1ec-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3b1ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b1ec-109">EXAMPLES</span></span>

### <span data-ttu-id="3b1ec-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b1ec-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3b1ec-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="3b1ec-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="3b1ec-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b1ec-112">PARAMETERS</span></span>

### <span data-ttu-id="3b1ec-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b1ec-113">-CdnEndpoint</span></span>
<span data-ttu-id="3b1ec-114">CDN uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="3b1ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1ec-115">-DefaultProfile</span></span>
<span data-ttu-id="3b1ec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3b1ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b1ec-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3b1ec-117">-EndpointName</span></span>
<span data-ttu-id="3b1ec-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3b1ec-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3b1ec-119">-ProfileName</span></span>
<span data-ttu-id="3b1ec-120">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3b1ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b1ec-122">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="3b1ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1ec-123">CommonParameters</span></span>
<span data-ttu-id="3b1ec-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b1ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1ec-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1ec-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b1ec-126">INPUTS</span></span>

### <span data-ttu-id="3b1ec-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b1ec-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="3b1ec-128">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b1ec-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="3b1ec-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b1ec-129">OUTPUTS</span></span>

### <span data-ttu-id="3b1ec-130">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3b1ec-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="3b1ec-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b1ec-131">NOTES</span></span>

## <span data-ttu-id="3b1ec-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b1ec-132">RELATED LINKS</span></span>
