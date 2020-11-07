---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: be7528f33bc51732c9345bbf7c9b718f590a8a5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761410"
---
# <span data-ttu-id="01a96-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="01a96-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="01a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01a96-102">SYNOPSIS</span></span>
<span data-ttu-id="01a96-103">CDN profili için desteklenen iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="01a96-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="01a96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01a96-104">SYNTAX</span></span>

### <span data-ttu-id="01a96-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01a96-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a96-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01a96-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01a96-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01a96-107">DESCRIPTION</span></span>
<span data-ttu-id="01a96-108">**Get-AzCdnProfileSupportedOptimizationType** cmdlet 'i geçerli profil için desteklenen en iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="01a96-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="01a96-109">Bir Kullanıcı, listelenen değerlerden en iyi duruma getirme türünde bir uç nokta oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="01a96-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="01a96-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01a96-110">EXAMPLES</span></span>

### <span data-ttu-id="01a96-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01a96-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="01a96-112">CDN profili için desteklenen iyileştirme türlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="01a96-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="01a96-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01a96-113">PARAMETERS</span></span>

### <span data-ttu-id="01a96-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="01a96-114">-CdnProfile</span></span>
<span data-ttu-id="01a96-115">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="01a96-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="01a96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a96-116">-DefaultProfile</span></span>
<span data-ttu-id="01a96-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01a96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a96-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="01a96-118">-ProfileName</span></span>
<span data-ttu-id="01a96-119">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="01a96-119">The name of the profile.</span></span>

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

### <span data-ttu-id="01a96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a96-120">-ResourceGroupName</span></span>
<span data-ttu-id="01a96-121">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="01a96-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="01a96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a96-122">CommonParameters</span></span>
<span data-ttu-id="01a96-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01a96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a96-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a96-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a96-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01a96-125">INPUTS</span></span>

### <span data-ttu-id="01a96-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="01a96-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="01a96-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01a96-127">OUTPUTS</span></span>

### <span data-ttu-id="01a96-128">Microsoft. Azure. Commands. CDN. model. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="01a96-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="01a96-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01a96-129">NOTES</span></span>

## <span data-ttu-id="01a96-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01a96-130">RELATED LINKS</span></span>
