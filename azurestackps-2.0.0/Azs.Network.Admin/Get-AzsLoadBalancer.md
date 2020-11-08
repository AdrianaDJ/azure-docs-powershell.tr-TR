---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935998"
---
# <span data-ttu-id="a8d73-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a8d73-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="a8d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d73-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d73-103">Tüm yük dengeleyicileri listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="a8d73-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a8d73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8d73-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8d73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8d73-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d73-106">Tüm yük dengeleyicileri listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="a8d73-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a8d73-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8d73-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d73-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8d73-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="a8d73-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8d73-109">PARAMETERS</span></span>

### <span data-ttu-id="a8d73-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d73-110">-DefaultProfile</span></span>
<span data-ttu-id="a8d73-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8d73-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d73-112">-Filtre</span><span class="sxs-lookup"><span data-stu-id="a8d73-112">-Filter</span></span>
<span data-ttu-id="a8d73-113">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="a8d73-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="a8d73-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="a8d73-114">-InlineCount</span></span>
<span data-ttu-id="a8d73-115">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="a8d73-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="a8d73-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a8d73-116">-OrderBy</span></span>
<span data-ttu-id="a8d73-117">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="a8d73-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="a8d73-118">-Atla</span><span class="sxs-lookup"><span data-stu-id="a8d73-118">-Skip</span></span>
<span data-ttu-id="a8d73-119">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="a8d73-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="a8d73-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a8d73-120">-SubscriptionId</span></span>
<span data-ttu-id="a8d73-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a8d73-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a8d73-122">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a8d73-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a8d73-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="a8d73-123">-Top</span></span>
<span data-ttu-id="a8d73-124">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="a8d73-124">OData top parameter.</span></span>

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

### <span data-ttu-id="a8d73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d73-125">CommonParameters</span></span>
<span data-ttu-id="a8d73-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8d73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d73-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a8d73-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d73-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8d73-128">INPUTS</span></span>

## <span data-ttu-id="a8d73-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8d73-129">OUTPUTS</span></span>

### <span data-ttu-id="a8d73-130">Microsoft. Azure. PowerShell. cmdlet. Ağyöneticisi. modeller. Api20150615.</span><span class="sxs-lookup"><span data-stu-id="a8d73-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="a8d73-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8d73-131">NOTES</span></span>

## <span data-ttu-id="a8d73-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8d73-132">RELATED LINKS</span></span>
