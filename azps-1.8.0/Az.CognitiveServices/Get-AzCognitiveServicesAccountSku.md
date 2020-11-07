---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: d041d18713efa4d094a46747a9697eb76dcea578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917535"
---
# <span data-ttu-id="fb2ae-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="fb2ae-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="fb2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2ae-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="fb2ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb2ae-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb2ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb2ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2ae-106">**Get-az, ınitialveservicesaccountsku** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="fb2ae-107">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="fb2ae-108">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="fb2ae-109">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="fb2ae-110">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="fb2ae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb2ae-111">EXAMPLES</span></span>

### <span data-ttu-id="fb2ae-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb2ae-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="fb2ae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb2ae-113">PARAMETERS</span></span>

### <span data-ttu-id="fb2ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2ae-114">-DefaultProfile</span></span>
<span data-ttu-id="fb2ae-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb2ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb2ae-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="fb2ae-116">-Location</span></span>
<span data-ttu-id="fb2ae-117">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="fb2ae-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="fb2ae-118">-Type</span></span>
<span data-ttu-id="fb2ae-119">Öğretici hizmetler hesap türü.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="fb2ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2ae-120">CommonParameters</span></span>
<span data-ttu-id="fb2ae-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb2ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2ae-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2ae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2ae-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb2ae-123">INPUTS</span></span>

### <span data-ttu-id="fb2ae-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fb2ae-124">System.String</span></span>

## <span data-ttu-id="fb2ae-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb2ae-125">OUTPUTS</span></span>

### <span data-ttu-id="fb2ae-126">Microsoft. Azure. Management. öğretici Bveservices. modeller. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="fb2ae-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="fb2ae-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb2ae-127">NOTES</span></span>

## <span data-ttu-id="fb2ae-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb2ae-128">RELATED LINKS</span></span>
