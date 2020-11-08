---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279556"
---
# <span data-ttu-id="2c631-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2c631-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="2c631-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c631-102">SYNOPSIS</span></span>
<span data-ttu-id="2c631-103">Blockzincirine üye için konsorsiyum üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="2c631-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2c631-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c631-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2c631-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c631-105">DESCRIPTION</span></span>
<span data-ttu-id="2c631-106">Blockzincirine üye için konsorsiyum üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="2c631-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2c631-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c631-107">EXAMPLES</span></span>

### <span data-ttu-id="2c631-108">Örnek 1: blockzincirine üye için konsorsiyum üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="2c631-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="2c631-109">Bu komut, blockzincirine üye için konsorsiyum üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="2c631-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2c631-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c631-110">PARAMETERS</span></span>

### <span data-ttu-id="2c631-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2c631-111">-BlockchainMemberName</span></span>
<span data-ttu-id="2c631-112">Blockzincir üye adı.</span><span class="sxs-lookup"><span data-stu-id="2c631-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="2c631-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c631-113">-DefaultProfile</span></span>
<span data-ttu-id="2c631-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c631-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c631-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c631-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c631-116">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2c631-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2c631-117">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c631-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2c631-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2c631-118">-SubscriptionId</span></span>
<span data-ttu-id="2c631-119">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimliğini alır.</span><span class="sxs-lookup"><span data-stu-id="2c631-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c631-120">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="2c631-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2c631-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c631-121">CommonParameters</span></span>
<span data-ttu-id="2c631-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c631-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c631-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c631-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c631-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c631-124">INPUTS</span></span>

## <span data-ttu-id="2c631-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c631-125">OUTPUTS</span></span>

### <span data-ttu-id="2c631-126">Microsoft. Azure. PowerShell. cmdlet. Blockzincirine. modeller. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2c631-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="2c631-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c631-127">NOTES</span></span>

<span data-ttu-id="2c631-128">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2c631-128">ALIASES</span></span>

## <span data-ttu-id="2c631-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c631-129">RELATED LINKS</span></span>

