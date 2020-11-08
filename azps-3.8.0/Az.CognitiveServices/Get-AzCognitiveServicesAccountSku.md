---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095793"
---
# <span data-ttu-id="51ddb-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="51ddb-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="51ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="51ddb-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="51ddb-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="51ddb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51ddb-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ddb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="51ddb-106">**Get-az, ınitialveservicesaccountsku** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="51ddb-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="51ddb-107">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="51ddb-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="51ddb-108">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="51ddb-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="51ddb-109">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="51ddb-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="51ddb-110">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="51ddb-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="51ddb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51ddb-111">EXAMPLES</span></span>

### <span data-ttu-id="51ddb-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51ddb-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="51ddb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51ddb-113">PARAMETERS</span></span>

### <span data-ttu-id="51ddb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ddb-114">-DefaultProfile</span></span>
<span data-ttu-id="51ddb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51ddb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51ddb-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="51ddb-116">-Location</span></span>
<span data-ttu-id="51ddb-117">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="51ddb-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="51ddb-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="51ddb-118">-Type</span></span>
<span data-ttu-id="51ddb-119">Öğretici hizmetler hesap türü.</span><span class="sxs-lookup"><span data-stu-id="51ddb-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="51ddb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ddb-120">CommonParameters</span></span>
<span data-ttu-id="51ddb-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51ddb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ddb-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51ddb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ddb-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51ddb-123">INPUTS</span></span>

### <span data-ttu-id="51ddb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="51ddb-124">System.String</span></span>

## <span data-ttu-id="51ddb-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51ddb-125">OUTPUTS</span></span>

### <span data-ttu-id="51ddb-126">Microsoft. Azure. Management. öğretici Bveservices. modeller. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="51ddb-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="51ddb-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51ddb-127">NOTES</span></span>

## <span data-ttu-id="51ddb-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51ddb-128">RELATED LINKS</span></span>