---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277633"
---
# <span data-ttu-id="45c0d-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="45c0d-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="45c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="45c0d-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="45c0d-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="45c0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45c0d-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45c0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="45c0d-106">**Get-az, ınitialveservicesaccountsku** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="45c0d-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="45c0d-107">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="45c0d-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="45c0d-108">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="45c0d-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="45c0d-109">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="45c0d-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="45c0d-110">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="45c0d-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="45c0d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45c0d-111">EXAMPLES</span></span>

### <span data-ttu-id="45c0d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45c0d-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="45c0d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45c0d-113">PARAMETERS</span></span>

### <span data-ttu-id="45c0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c0d-114">-DefaultProfile</span></span>
<span data-ttu-id="45c0d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45c0d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45c0d-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="45c0d-116">-Location</span></span>
<span data-ttu-id="45c0d-117">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="45c0d-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="45c0d-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="45c0d-118">-Type</span></span>
<span data-ttu-id="45c0d-119">Öğretici hizmetler hesap türü.</span><span class="sxs-lookup"><span data-stu-id="45c0d-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="45c0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c0d-120">CommonParameters</span></span>
<span data-ttu-id="45c0d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45c0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c0d-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45c0d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c0d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45c0d-123">INPUTS</span></span>

### <span data-ttu-id="45c0d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="45c0d-124">System.String</span></span>

## <span data-ttu-id="45c0d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45c0d-125">OUTPUTS</span></span>

### <span data-ttu-id="45c0d-126">Microsoft. Azure. Management. öğretici Bveservices. modeller. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="45c0d-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="45c0d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45c0d-127">NOTES</span></span>

## <span data-ttu-id="45c0d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45c0d-128">RELATED LINKS</span></span>
