---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592327"
---
# <span data-ttu-id="37291-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="37291-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="37291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37291-102">SYNOPSIS</span></span>
<span data-ttu-id="37291-103">Bir hesap için kullanılabilir STB 'leri alır.</span><span class="sxs-lookup"><span data-stu-id="37291-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37291-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37291-104">SYNTAX</span></span>

### <span data-ttu-id="37291-105">GetSkusWithAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37291-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37291-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="37291-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37291-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37291-107">DESCRIPTION</span></span>
<span data-ttu-id="37291-108">**Get-Azurermöğretici Iveservicesaccountstb** cmdlet 'i, bir öğretici hizmet hesabı Için kullanılabilir SKU 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="37291-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="37291-109">SKU, bir hesabın katman planıdır.</span><span class="sxs-lookup"><span data-stu-id="37291-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="37291-110">Hesabın fiyatını, çağrı sınırını ve oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="37291-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="37291-111">F0 SKU 'SU ücretsiz bir katmandır.</span><span class="sxs-lookup"><span data-stu-id="37291-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="37291-112">Ücretli katmanlar S0, S1, S2 ve bu gibi.</span><span class="sxs-lookup"><span data-stu-id="37291-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="37291-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37291-113">EXAMPLES</span></span>

### <span data-ttu-id="37291-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37291-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="37291-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37291-115">PARAMETERS</span></span>

### <span data-ttu-id="37291-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37291-116">-DefaultProfile</span></span>
<span data-ttu-id="37291-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="37291-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37291-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="37291-118">-Location</span></span>
<span data-ttu-id="37291-119">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="37291-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37291-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="37291-120">-Name</span></span>
<span data-ttu-id="37291-121">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37291-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37291-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37291-122">-ResourceGroupName</span></span>
<span data-ttu-id="37291-123">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37291-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37291-124">-Tür</span><span class="sxs-lookup"><span data-stu-id="37291-124">-Type</span></span>
<span data-ttu-id="37291-125">Öğretici hizmetler hesap türü.</span><span class="sxs-lookup"><span data-stu-id="37291-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37291-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37291-126">CommonParameters</span></span>
<span data-ttu-id="37291-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37291-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37291-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37291-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37291-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37291-129">INPUTS</span></span>

### <span data-ttu-id="37291-130">System. String</span><span class="sxs-lookup"><span data-stu-id="37291-130">System.String</span></span>

## <span data-ttu-id="37291-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37291-131">OUTPUTS</span></span>

### <span data-ttu-id="37291-132">Microsoft. Azure. Commands. Management. öğretici.</span><span class="sxs-lookup"><span data-stu-id="37291-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="37291-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37291-133">NOTES</span></span>

## <span data-ttu-id="37291-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37291-134">RELATED LINKS</span></span>
