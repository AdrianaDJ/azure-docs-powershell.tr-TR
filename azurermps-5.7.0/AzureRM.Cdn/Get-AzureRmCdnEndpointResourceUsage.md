---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594138"
---
# <span data-ttu-id="56706-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="56706-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="56706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56706-102">SYNOPSIS</span></span>
<span data-ttu-id="56706-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="56706-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56706-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56706-104">SYNTAX</span></span>

### <span data-ttu-id="56706-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56706-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56706-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56706-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56706-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56706-107">DESCRIPTION</span></span>
<span data-ttu-id="56706-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="56706-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="56706-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56706-109">EXAMPLES</span></span>

### <span data-ttu-id="56706-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56706-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="56706-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="56706-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="56706-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56706-112">PARAMETERS</span></span>

### <span data-ttu-id="56706-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56706-113">-CdnEndpoint</span></span>
<span data-ttu-id="56706-114">CDN uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="56706-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="56706-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56706-115">-DefaultProfile</span></span>
<span data-ttu-id="56706-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56706-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56706-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="56706-117">-EndpointName</span></span>
<span data-ttu-id="56706-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="56706-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="56706-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="56706-119">-ProfileName</span></span>
<span data-ttu-id="56706-120">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="56706-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="56706-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56706-121">-ResourceGroupName</span></span>
<span data-ttu-id="56706-122">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="56706-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="56706-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56706-123">CommonParameters</span></span>
<span data-ttu-id="56706-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56706-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56706-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56706-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56706-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56706-126">INPUTS</span></span>

### <span data-ttu-id="56706-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="56706-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="56706-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56706-128">OUTPUTS</span></span>

### <span data-ttu-id="56706-129">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="56706-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="56706-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56706-130">NOTES</span></span>

## <span data-ttu-id="56706-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56706-131">RELATED LINKS</span></span>

