---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591112"
---
# <span data-ttu-id="c114f-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="c114f-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="c114f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c114f-102">SYNOPSIS</span></span>
<span data-ttu-id="c114f-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="c114f-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c114f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c114f-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c114f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c114f-105">DESCRIPTION</span></span>
<span data-ttu-id="c114f-106">**Get-Azurermöğretici Iveservicesaccountstb** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="c114f-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="c114f-107">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="c114f-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="c114f-108">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c114f-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="c114f-109">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="c114f-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="c114f-110">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="c114f-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="c114f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c114f-111">EXAMPLES</span></span>

## <span data-ttu-id="c114f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c114f-112">PARAMETERS</span></span>

### <span data-ttu-id="c114f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c114f-113">-Name</span></span>
<span data-ttu-id="c114f-114">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c114f-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c114f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c114f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c114f-116">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c114f-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c114f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c114f-117">-DefaultProfile</span></span>
<span data-ttu-id="c114f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c114f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c114f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c114f-119">CommonParameters</span></span>
<span data-ttu-id="c114f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c114f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c114f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c114f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c114f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c114f-122">INPUTS</span></span>

## <span data-ttu-id="c114f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c114f-123">OUTPUTS</span></span>

### <span data-ttu-id="c114f-124">Microsoft. Azure. Commands. Management. öğretici.</span><span class="sxs-lookup"><span data-stu-id="c114f-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="c114f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c114f-125">NOTES</span></span>

## <span data-ttu-id="c114f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c114f-126">RELATED LINKS</span></span>

