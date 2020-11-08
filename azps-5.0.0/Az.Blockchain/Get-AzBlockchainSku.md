---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279551"
---
# <span data-ttu-id="d9f3a-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="d9f3a-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="d9f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f3a-103">Kaynak türünün STB 'Larını listeler.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="d9f3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9f3a-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9f3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="d9f3a-106">Kaynak türünün STB 'Larını listeler.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="d9f3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="d9f3a-108">Örnek 1: aboneliğin liste SKU 'SU</span><span class="sxs-lookup"><span data-stu-id="d9f3a-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="d9f3a-109">Bu komut, bir aboneliğin SKU 'SU listeler.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="d9f3a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="d9f3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f3a-111">-DefaultProfile</span></span>
<span data-ttu-id="d9f3a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f3a-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d9f3a-113">-SubscriptionId</span></span>
<span data-ttu-id="d9f3a-114">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9f3a-115">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9f3a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f3a-116">CommonParameters</span></span>
<span data-ttu-id="d9f3a-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f3a-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9f3a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f3a-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9f3a-119">INPUTS</span></span>

## <span data-ttu-id="d9f3a-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9f3a-120">OUTPUTS</span></span>

### <span data-ttu-id="d9f3a-121">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıresourcetypesku</span><span class="sxs-lookup"><span data-stu-id="d9f3a-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="d9f3a-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9f3a-122">NOTES</span></span>

<span data-ttu-id="d9f3a-123">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d9f3a-123">ALIASES</span></span>

## <span data-ttu-id="d9f3a-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9f3a-124">RELATED LINKS</span></span>

