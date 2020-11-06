---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592795"
---
# <span data-ttu-id="02ed3-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="02ed3-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="02ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="02ed3-103">CDN profili için desteklenen iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="02ed3-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02ed3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02ed3-104">SYNTAX</span></span>

### <span data-ttu-id="02ed3-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02ed3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ed3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ed3-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ed3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="02ed3-107">DESCRIPTION</span></span>
<span data-ttu-id="02ed3-108">**Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet 'i geçerli profil için desteklenen en iyileştirme türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="02ed3-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="02ed3-109">Bir Kullanıcı, listelenen değerlerden en iyi duruma getirme türünde bir uç nokta oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="02ed3-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="02ed3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02ed3-110">EXAMPLES</span></span>

### <span data-ttu-id="02ed3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02ed3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="02ed3-112">CDN profili için desteklenen iyileştirme türlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="02ed3-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="02ed3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02ed3-113">PARAMETERS</span></span>

### <span data-ttu-id="02ed3-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="02ed3-114">-CdnProfile</span></span>
<span data-ttu-id="02ed3-115">Azure CDN profil nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02ed3-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="02ed3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ed3-116">-DefaultProfile</span></span>
<span data-ttu-id="02ed3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02ed3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ed3-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="02ed3-118">-ProfileName</span></span>
<span data-ttu-id="02ed3-119">Profilin adı.</span><span class="sxs-lookup"><span data-stu-id="02ed3-119">The name of the profile.</span></span>

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

### <span data-ttu-id="02ed3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ed3-120">-ResourceGroupName</span></span>
<span data-ttu-id="02ed3-121">Profilin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="02ed3-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="02ed3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ed3-122">CommonParameters</span></span>
<span data-ttu-id="02ed3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02ed3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ed3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ed3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ed3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02ed3-125">INPUTS</span></span>

### <span data-ttu-id="02ed3-126">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="02ed3-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="02ed3-127">Parametreler: Cdnprofıle (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02ed3-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="02ed3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02ed3-128">OUTPUTS</span></span>

### <span data-ttu-id="02ed3-129">Microsoft. Azure. Commands. CDN. model. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="02ed3-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="02ed3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02ed3-130">NOTES</span></span>

## <span data-ttu-id="02ed3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02ed3-131">RELATED LINKS</span></span>
