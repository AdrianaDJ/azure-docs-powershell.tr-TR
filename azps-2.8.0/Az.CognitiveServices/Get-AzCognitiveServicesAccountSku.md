---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 7fe9a0e87d656063491d2787ad8afcdeb6fef4f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753028"
---
# <span data-ttu-id="f0a2c-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="f0a2c-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="f0a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a2c-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="f0a2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0a2c-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a2c-106">**Get-az, ınitialveservicesaccountsku** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="f0a2c-107">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="f0a2c-108">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="f0a2c-109">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="f0a2c-110">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="f0a2c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0a2c-111">EXAMPLES</span></span>

### <span data-ttu-id="f0a2c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0a2c-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="f0a2c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0a2c-113">PARAMETERS</span></span>

### <span data-ttu-id="f0a2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a2c-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a2c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f0a2c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0a2c-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="f0a2c-116">-Location</span></span>
<span data-ttu-id="f0a2c-117">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="f0a2c-118">-Type</span></span>
<span data-ttu-id="f0a2c-119">Öğretici hizmetler hesap türü.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a2c-120">CommonParameters</span></span>
<span data-ttu-id="f0a2c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a2c-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0a2c-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a2c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0a2c-123">INPUTS</span></span>

### <span data-ttu-id="f0a2c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f0a2c-124">System.String</span></span>

## <span data-ttu-id="f0a2c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0a2c-125">OUTPUTS</span></span>

### <span data-ttu-id="f0a2c-126">Microsoft. Azure. Management. öğretici Bveservices. modeller. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="f0a2c-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="f0a2c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0a2c-127">NOTES</span></span>

## <span data-ttu-id="f0a2c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0a2c-128">RELATED LINKS</span></span>
