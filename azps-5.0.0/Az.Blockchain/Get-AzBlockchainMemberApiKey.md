---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279557"
---
# <span data-ttu-id="81441-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="81441-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="81441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81441-102">SYNOPSIS</span></span>
<span data-ttu-id="81441-103">Blockzincirine üye için API anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="81441-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="81441-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81441-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81441-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81441-105">DESCRIPTION</span></span>
<span data-ttu-id="81441-106">Blockzincirine üye için API anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="81441-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="81441-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81441-107">EXAMPLES</span></span>

### <span data-ttu-id="81441-108">Örnek 1: List blockzincirine API anahtarları</span><span class="sxs-lookup"><span data-stu-id="81441-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="81441-109">Bu komut, blockzincirine üyesi için API anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="81441-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="81441-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81441-110">PARAMETERS</span></span>

### <span data-ttu-id="81441-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="81441-111">-BlockchainMemberName</span></span>
<span data-ttu-id="81441-112">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="81441-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="81441-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81441-113">-DefaultProfile</span></span>
<span data-ttu-id="81441-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81441-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81441-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81441-115">-ResourceGroupName</span></span>
<span data-ttu-id="81441-116">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="81441-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="81441-117">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81441-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="81441-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="81441-118">-SubscriptionId</span></span>
<span data-ttu-id="81441-119">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="81441-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="81441-120">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="81441-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81441-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="81441-121">-Confirm</span></span>
<span data-ttu-id="81441-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81441-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81441-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81441-123">-WhatIf</span></span>
<span data-ttu-id="81441-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81441-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81441-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81441-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81441-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81441-126">CommonParameters</span></span>
<span data-ttu-id="81441-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81441-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81441-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="81441-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81441-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81441-129">INPUTS</span></span>

## <span data-ttu-id="81441-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81441-130">OUTPUTS</span></span>

### <span data-ttu-id="81441-131">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıapıkey</span><span class="sxs-lookup"><span data-stu-id="81441-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="81441-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81441-132">NOTES</span></span>

<span data-ttu-id="81441-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="81441-133">ALIASES</span></span>

## <span data-ttu-id="81441-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81441-134">RELATED LINKS</span></span>

