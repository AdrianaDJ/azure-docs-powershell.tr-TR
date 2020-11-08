---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110051"
---
# <span data-ttu-id="56e25-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="56e25-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="56e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e25-102">SYNOPSIS</span></span>
<span data-ttu-id="56e25-103">Kaynak türünün STB 'Larını listeler.</span><span class="sxs-lookup"><span data-stu-id="56e25-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="56e25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56e25-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="56e25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56e25-105">DESCRIPTION</span></span>
<span data-ttu-id="56e25-106">Kaynak türünün STB 'Larını listeler.</span><span class="sxs-lookup"><span data-stu-id="56e25-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="56e25-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56e25-107">EXAMPLES</span></span>

### <span data-ttu-id="56e25-108">Örnek 1: aboneliğin liste SKU 'SU</span><span class="sxs-lookup"><span data-stu-id="56e25-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="56e25-109">Bu komut, bir aboneliğin SKU 'SU listeler.</span><span class="sxs-lookup"><span data-stu-id="56e25-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="56e25-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56e25-110">PARAMETERS</span></span>

### <span data-ttu-id="56e25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e25-111">-DefaultProfile</span></span>
<span data-ttu-id="56e25-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56e25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e25-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="56e25-113">-SubscriptionId</span></span>
<span data-ttu-id="56e25-114">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="56e25-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="56e25-115">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="56e25-115">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e25-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e25-116">CommonParameters</span></span>
<span data-ttu-id="56e25-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56e25-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e25-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56e25-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e25-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56e25-119">INPUTS</span></span>

## <span data-ttu-id="56e25-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56e25-120">OUTPUTS</span></span>

### <span data-ttu-id="56e25-121">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıresourcetypesku</span><span class="sxs-lookup"><span data-stu-id="56e25-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="56e25-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56e25-122">NOTES</span></span>

<span data-ttu-id="56e25-123">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="56e25-123">ALIASES</span></span>

## <span data-ttu-id="56e25-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56e25-124">RELATED LINKS</span></span>

