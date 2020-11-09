---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322201"
---
# <span data-ttu-id="30b90-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="30b90-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="30b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30b90-102">SYNOPSIS</span></span>
<span data-ttu-id="30b90-103">Küme Oluştur</span><span class="sxs-lookup"><span data-stu-id="30b90-103">Create cluster</span></span>

## <span data-ttu-id="30b90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30b90-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30b90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30b90-105">DESCRIPTION</span></span>

<span data-ttu-id="30b90-106">Küme Oluştur</span><span class="sxs-lookup"><span data-stu-id="30b90-106">Create cluster</span></span>

## <span data-ttu-id="30b90-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30b90-107">EXAMPLES</span></span>

### <span data-ttu-id="30b90-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30b90-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="30b90-109">Küme Oluştur</span><span class="sxs-lookup"><span data-stu-id="30b90-109">Create cluster</span></span>

## <span data-ttu-id="30b90-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30b90-110">PARAMETERS</span></span>

### <span data-ttu-id="30b90-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="30b90-111">-AsJob</span></span>
<span data-ttu-id="30b90-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="30b90-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30b90-113">-ClusterName</span></span>
<span data-ttu-id="30b90-114">Küme adı.</span><span class="sxs-lookup"><span data-stu-id="30b90-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b90-115">-DefaultProfile</span></span>
<span data-ttu-id="30b90-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30b90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="30b90-117">-IdentityType</span></span>
<span data-ttu-id="30b90-118">kimlik türü; değer ' SystemAssigned ', ' none ' olabilir.</span><span class="sxs-lookup"><span data-stu-id="30b90-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="30b90-119">-Location</span></span>
<span data-ttu-id="30b90-120">Kümenin dağıtılacağı coğrafi bölge.</span><span class="sxs-lookup"><span data-stu-id="30b90-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30b90-121">-ResourceGroupName</span></span>
<span data-ttu-id="30b90-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="30b90-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-123">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="30b90-123">-SkuCapacity</span></span>
<span data-ttu-id="30b90-124">STB kapasitesi, değerin 100 ve 1000-2000 aralığında olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="30b90-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="30b90-125">-SkuName</span></span>
<span data-ttu-id="30b90-126">SKU adı, şimdi yalnızca ' Capacityreservatıon ' olabilir</span><span class="sxs-lookup"><span data-stu-id="30b90-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="30b90-127">-Tags</span></span>
<span data-ttu-id="30b90-128">Kümenin etiketleri</span><span class="sxs-lookup"><span data-stu-id="30b90-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="30b90-129">-Confirm</span></span>
<span data-ttu-id="30b90-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30b90-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30b90-131">-WhatIf</span></span>
<span data-ttu-id="30b90-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30b90-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30b90-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30b90-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30b90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b90-134">CommonParameters</span></span>
<span data-ttu-id="30b90-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30b90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b90-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30b90-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b90-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30b90-137">INPUTS</span></span>

### <span data-ttu-id="30b90-138">System. String</span><span class="sxs-lookup"><span data-stu-id="30b90-138">System.String</span></span>

## <span data-ttu-id="30b90-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30b90-139">OUTPUTS</span></span>

### <span data-ttu-id="30b90-140">Microsoft. Azure. Commands. Operationalınsights. model. PSCluster</span><span class="sxs-lookup"><span data-stu-id="30b90-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="30b90-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30b90-141">NOTES</span></span>

## <span data-ttu-id="30b90-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30b90-142">RELATED LINKS</span></span>
