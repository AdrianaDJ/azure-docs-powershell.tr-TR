---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279546"
---
# <span data-ttu-id="41468-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="41468-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="41468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41468-102">SYNOPSIS</span></span>
<span data-ttu-id="41468-103">İşlem düğümünün API anahtarlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="41468-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="41468-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41468-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="41468-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41468-105">DESCRIPTION</span></span>
<span data-ttu-id="41468-106">İşlem düğümünün API anahtarlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="41468-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="41468-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41468-107">EXAMPLES</span></span>

### <span data-ttu-id="41468-108">Örnek 1: işlem düğümü için API anahtarları listesi</span><span class="sxs-lookup"><span data-stu-id="41468-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="41468-109">Bu komut, işlem düğümünün API anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="41468-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="41468-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41468-110">PARAMETERS</span></span>

### <span data-ttu-id="41468-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="41468-111">-BlockchainMemberName</span></span>
<span data-ttu-id="41468-112">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="41468-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="41468-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41468-113">-DefaultProfile</span></span>
<span data-ttu-id="41468-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41468-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41468-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41468-115">-ResourceGroupName</span></span>
<span data-ttu-id="41468-116">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41468-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="41468-117">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41468-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="41468-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="41468-118">-SubscriptionId</span></span>
<span data-ttu-id="41468-119">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="41468-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="41468-120">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="41468-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41468-121">-Transactiondüğüdynamicsnav:////runpage</span><span class="sxs-lookup"><span data-stu-id="41468-121">-TransactionNodeName</span></span>
<span data-ttu-id="41468-122">İşlem düğümü adı.</span><span class="sxs-lookup"><span data-stu-id="41468-122">Transaction node name.</span></span>

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

### <span data-ttu-id="41468-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="41468-123">-Confirm</span></span>
<span data-ttu-id="41468-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41468-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41468-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41468-125">-WhatIf</span></span>
<span data-ttu-id="41468-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41468-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41468-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41468-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41468-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41468-128">CommonParameters</span></span>
<span data-ttu-id="41468-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41468-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41468-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41468-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41468-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41468-131">INPUTS</span></span>

## <span data-ttu-id="41468-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41468-132">OUTPUTS</span></span>

### <span data-ttu-id="41468-133">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. ıapıkey</span><span class="sxs-lookup"><span data-stu-id="41468-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="41468-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41468-134">NOTES</span></span>

<span data-ttu-id="41468-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="41468-135">ALIASES</span></span>

## <span data-ttu-id="41468-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41468-136">RELATED LINKS</span></span>

