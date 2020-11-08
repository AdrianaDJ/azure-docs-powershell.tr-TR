---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273697"
---
# <span data-ttu-id="92914-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="92914-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="92914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92914-102">SYNOPSIS</span></span>
<span data-ttu-id="92914-103">Kaynak adının kullanılabilir olup olmadığını denetlemek için.</span><span class="sxs-lookup"><span data-stu-id="92914-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="92914-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92914-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92914-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92914-105">DESCRIPTION</span></span>
<span data-ttu-id="92914-106">Kaynak adının kullanılabilir olup olmadığını denetlemek için.</span><span class="sxs-lookup"><span data-stu-id="92914-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="92914-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92914-107">EXAMPLES</span></span>

### <span data-ttu-id="92914-108">Örnek 1: kaynak adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="92914-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="92914-109">Komut, kaynak adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="92914-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="92914-110">Örnek 2: kaynak adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="92914-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="92914-111">Komut, kaynak adının kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="92914-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="92914-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92914-112">PARAMETERS</span></span>

### <span data-ttu-id="92914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92914-113">-DefaultProfile</span></span>
<span data-ttu-id="92914-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92914-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92914-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="92914-115">-Location</span></span>
<span data-ttu-id="92914-116">Konum adı.</span><span class="sxs-lookup"><span data-stu-id="92914-116">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="92914-117">-Name</span></span>
<span data-ttu-id="92914-118">Denetlenecek adı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92914-118">Gets or sets the name to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="92914-119">-SubscriptionId</span></span>
<span data-ttu-id="92914-120">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="92914-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="92914-121">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="92914-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-122">-Tür</span><span class="sxs-lookup"><span data-stu-id="92914-122">-Type</span></span>
<span data-ttu-id="92914-123">Denetlenecek kaynağın türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92914-123">Gets or sets the type of the resource to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="92914-124">-Confirm</span></span>
<span data-ttu-id="92914-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92914-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92914-126">-WhatIf</span></span>
<span data-ttu-id="92914-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92914-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92914-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92914-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92914-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92914-129">CommonParameters</span></span>
<span data-ttu-id="92914-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92914-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92914-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92914-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92914-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92914-132">INPUTS</span></span>

## <span data-ttu-id="92914-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92914-133">OUTPUTS</span></span>

### <span data-ttu-id="92914-134">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="92914-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="92914-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92914-135">NOTES</span></span>

<span data-ttu-id="92914-136">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="92914-136">ALIASES</span></span>

## <span data-ttu-id="92914-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92914-137">RELATED LINKS</span></span>

