---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935988"
---
# <span data-ttu-id="510e2-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="510e2-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="510e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="510e2-102">SYNOPSIS</span></span>
<span data-ttu-id="510e2-103">Tüm sanal ağların bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="510e2-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="510e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="510e2-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="510e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="510e2-105">DESCRIPTION</span></span>
<span data-ttu-id="510e2-106">Tüm sanal ağların bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="510e2-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="510e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="510e2-107">EXAMPLES</span></span>

### <span data-ttu-id="510e2-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="510e2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="510e2-109">Azure yığın damgası için sanal ağların listesini döndürme.</span><span class="sxs-lookup"><span data-stu-id="510e2-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="510e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="510e2-110">PARAMETERS</span></span>

### <span data-ttu-id="510e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510e2-111">-DefaultProfile</span></span>
<span data-ttu-id="510e2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="510e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="510e2-113">-Filtre</span><span class="sxs-lookup"><span data-stu-id="510e2-113">-Filter</span></span>
<span data-ttu-id="510e2-114">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="510e2-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="510e2-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="510e2-115">-InlineCount</span></span>
<span data-ttu-id="510e2-116">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="510e2-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="510e2-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="510e2-117">-OrderBy</span></span>
<span data-ttu-id="510e2-118">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="510e2-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="510e2-119">-Atla</span><span class="sxs-lookup"><span data-stu-id="510e2-119">-Skip</span></span>
<span data-ttu-id="510e2-120">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="510e2-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="510e2-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="510e2-121">-SubscriptionId</span></span>
<span data-ttu-id="510e2-122">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="510e2-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="510e2-123">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="510e2-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="510e2-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="510e2-124">-Top</span></span>
<span data-ttu-id="510e2-125">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="510e2-125">OData top parameter.</span></span>

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

### <span data-ttu-id="510e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510e2-126">CommonParameters</span></span>
<span data-ttu-id="510e2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="510e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510e2-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="510e2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510e2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="510e2-129">INPUTS</span></span>

## <span data-ttu-id="510e2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="510e2-130">OUTPUTS</span></span>

### <span data-ttu-id="510e2-131">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. modeller. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="510e2-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="510e2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="510e2-132">NOTES</span></span>

## <span data-ttu-id="510e2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="510e2-133">RELATED LINKS</span></span>
