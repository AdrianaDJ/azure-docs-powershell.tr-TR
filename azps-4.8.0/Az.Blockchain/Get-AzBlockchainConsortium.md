---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108486"
---
# <span data-ttu-id="b99a2-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="b99a2-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="b99a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b99a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b99a2-103">Bir abonelik için sağlanan kullanılabilir bir yol listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="b99a2-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="b99a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b99a2-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b99a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b99a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b99a2-106">Bir abonelik için sağlanan kullanılabilir bir yol listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="b99a2-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="b99a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b99a2-107">EXAMPLES</span></span>

### <span data-ttu-id="b99a2-108">Örnek 1: Blockzincirine yönelik çağrı alma.</span><span class="sxs-lookup"><span data-stu-id="b99a2-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="b99a2-109">Bu komut, belirli bir konum için bir aboneliğin altındaki uyumu listeler.</span><span class="sxs-lookup"><span data-stu-id="b99a2-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="b99a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b99a2-110">PARAMETERS</span></span>

### <span data-ttu-id="b99a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99a2-111">-DefaultProfile</span></span>
<span data-ttu-id="b99a2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b99a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b99a2-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="b99a2-113">-Location</span></span>
<span data-ttu-id="b99a2-114">Konum adı.</span><span class="sxs-lookup"><span data-stu-id="b99a2-114">Location Name.</span></span>

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

### <span data-ttu-id="b99a2-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b99a2-115">-SubscriptionId</span></span>
<span data-ttu-id="b99a2-116">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="b99a2-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b99a2-117">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="b99a2-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b99a2-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b99a2-118">-Confirm</span></span>
<span data-ttu-id="b99a2-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b99a2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b99a2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b99a2-120">-WhatIf</span></span>
<span data-ttu-id="b99a2-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b99a2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b99a2-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b99a2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b99a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99a2-123">CommonParameters</span></span>
<span data-ttu-id="b99a2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b99a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99a2-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b99a2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99a2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b99a2-126">INPUTS</span></span>

## <span data-ttu-id="b99a2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b99a2-127">OUTPUTS</span></span>

### <span data-ttu-id="b99a2-128">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="b99a2-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="b99a2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b99a2-129">NOTES</span></span>

<span data-ttu-id="b99a2-130">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b99a2-130">ALIASES</span></span>

## <span data-ttu-id="b99a2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b99a2-131">RELATED LINKS</span></span>

