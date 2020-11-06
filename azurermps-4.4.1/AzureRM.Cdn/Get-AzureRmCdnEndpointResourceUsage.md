---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595018"
---
# <span data-ttu-id="e817b-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e817b-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="e817b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e817b-102">SYNOPSIS</span></span>
<span data-ttu-id="e817b-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="e817b-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e817b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e817b-104">SYNTAX</span></span>

### <span data-ttu-id="e817b-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e817b-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e817b-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="e817b-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e817b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e817b-107">DESCRIPTION</span></span>
<span data-ttu-id="e817b-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="e817b-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e817b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e817b-109">EXAMPLES</span></span>

### <span data-ttu-id="e817b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e817b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e817b-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="e817b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e817b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e817b-112">PARAMETERS</span></span>

### <span data-ttu-id="e817b-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e817b-113">-CdnEndpoint</span></span>
<span data-ttu-id="e817b-114">CDN uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e817b-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="e817b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e817b-115">-EndpointName</span></span>
<span data-ttu-id="e817b-116">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="e817b-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e817b-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e817b-117">-ProfileName</span></span>
<span data-ttu-id="e817b-118">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="e817b-118">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e817b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e817b-119">-ResourceGroupName</span></span>
<span data-ttu-id="e817b-120">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e817b-120">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="e817b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e817b-121">-DefaultProfile</span></span>
<span data-ttu-id="e817b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e817b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e817b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e817b-123">CommonParameters</span></span>
<span data-ttu-id="e817b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e817b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e817b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e817b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e817b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e817b-126">INPUTS</span></span>

### <span data-ttu-id="e817b-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e817b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e817b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e817b-128">OUTPUTS</span></span>

### <span data-ttu-id="e817b-129">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e817b-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e817b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e817b-130">NOTES</span></span>

## <span data-ttu-id="e817b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e817b-131">RELATED LINKS</span></span>

