---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095964"
---
# <span data-ttu-id="e2264-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="e2264-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="e2264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2264-102">SYNOPSIS</span></span>
<span data-ttu-id="e2264-103">CDN profili için desteklenen iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2264-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="e2264-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2264-104">SYNTAX</span></span>

### <span data-ttu-id="e2264-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2264-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2264-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2264-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2264-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2264-107">DESCRIPTION</span></span>
<span data-ttu-id="e2264-108">**Get-AzCdnProfileSupportedOptimizationType** cmdlet 'i geçerli profil için desteklenen en iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2264-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="e2264-109">Bir Kullanıcı, listelenen değerlerden en iyi duruma getirme türünde bir uç nokta oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="e2264-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="e2264-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2264-110">EXAMPLES</span></span>

### <span data-ttu-id="e2264-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2264-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="e2264-112">CDN profili için desteklenen iyileştirme türlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="e2264-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="e2264-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2264-113">PARAMETERS</span></span>

### <span data-ttu-id="e2264-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e2264-114">-CdnProfile</span></span>
<span data-ttu-id="e2264-115">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e2264-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2264-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2264-116">-DefaultProfile</span></span>
<span data-ttu-id="e2264-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2264-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2264-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e2264-118">-ProfileName</span></span>
<span data-ttu-id="e2264-119">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="e2264-119">The name of the profile.</span></span>

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

### <span data-ttu-id="e2264-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2264-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2264-121">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e2264-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e2264-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2264-122">CommonParameters</span></span>
<span data-ttu-id="e2264-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2264-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2264-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2264-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2264-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2264-125">INPUTS</span></span>

### <span data-ttu-id="e2264-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e2264-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e2264-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2264-127">OUTPUTS</span></span>

### <span data-ttu-id="e2264-128">Microsoft. Azure. Commands. CDN. model. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="e2264-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="e2264-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2264-129">NOTES</span></span>

## <span data-ttu-id="e2264-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2264-130">RELATED LINKS</span></span>