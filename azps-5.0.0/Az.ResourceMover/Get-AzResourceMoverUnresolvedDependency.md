---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324334"
---
# <span data-ttu-id="d14a1-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="d14a1-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="d14a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d14a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d14a1-103">Çözülmemiş bağımlılıkların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d14a1-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d14a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d14a1-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d14a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d14a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d14a1-106">Çözülmemiş bağımlılıkların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d14a1-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="d14a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d14a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d14a1-108">Örnek 1: çözümlenmemiş bağımlı kaynakların listesini alma</span><span class="sxs-lookup"><span data-stu-id="d14a1-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="d14a1-109">Bir taşıma koleksiyonu için çözümlenmemiş bağımlı kaynakların listesini alma.</span><span class="sxs-lookup"><span data-stu-id="d14a1-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="d14a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d14a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d14a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14a1-111">-DefaultProfile</span></span>
<span data-ttu-id="d14a1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d14a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d14a1-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d14a1-113">-MoveCollectionName</span></span>
<span data-ttu-id="d14a1-114">Koleksiyon adını taşıma.</span><span class="sxs-lookup"><span data-stu-id="d14a1-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d14a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="d14a1-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d14a1-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d14a1-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d14a1-117">-SubscriptionId</span></span>
<span data-ttu-id="d14a1-118">Abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d14a1-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="d14a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14a1-119">CommonParameters</span></span>
<span data-ttu-id="d14a1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d14a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14a1-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d14a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14a1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d14a1-122">INPUTS</span></span>

## <span data-ttu-id="d14a1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d14a1-123">OUTPUTS</span></span>

### <span data-ttu-id="d14a1-124">Microsoft. Azure. PowerShell. cmdlet. Kaynaktaşıyıcısı. modeller. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="d14a1-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="d14a1-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d14a1-125">NOTES</span></span>

<span data-ttu-id="d14a1-126">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d14a1-126">ALIASES</span></span>

## <span data-ttu-id="d14a1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d14a1-127">RELATED LINKS</span></span>

