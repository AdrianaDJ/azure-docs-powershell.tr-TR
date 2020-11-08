---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268417"
---
# <span data-ttu-id="8a3b8-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="8a3b8-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="8a3b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3b8-103">kümeyi Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="8a3b8-103">update cluster</span></span>

## <span data-ttu-id="8a3b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a3b8-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a3b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a3b8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a3b8-106">kümeyi Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="8a3b8-106">update cluster</span></span>

## <span data-ttu-id="8a3b8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a3b8-107">EXAMPLES</span></span>

### <span data-ttu-id="8a3b8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a3b8-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="8a3b8-109">anahtarı Anahtar Kasası özellikleri ve SKU ile Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="8a3b8-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="8a3b8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a3b8-110">PARAMETERS</span></span>

### <span data-ttu-id="8a3b8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="8a3b8-111">-AsJob</span></span>
<span data-ttu-id="8a3b8-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8a3b8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a3b8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8a3b8-113">-ClusterName</span></span>
<span data-ttu-id="8a3b8-114">Küme adı.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-114">The cluster name.</span></span>

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

### <span data-ttu-id="8a3b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3b8-115">-DefaultProfile</span></span>
<span data-ttu-id="8a3b8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a3b8-117">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="8a3b8-117">-KeyName</span></span>
<span data-ttu-id="8a3b8-118">Anahtar adı</span><span class="sxs-lookup"><span data-stu-id="8a3b8-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3b8-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8a3b8-119">-KeyVaultUri</span></span>
<span data-ttu-id="8a3b8-120">Bu tuş Kasası için Anahtar Kasası URI, "koruma</span><span class="sxs-lookup"><span data-stu-id="8a3b8-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3b8-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8a3b8-121">-KeyVersion</span></span>
<span data-ttu-id="8a3b8-122">Anahtar sürümü</span><span class="sxs-lookup"><span data-stu-id="8a3b8-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a3b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a3b8-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-124">The resource group name.</span></span>

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

### <span data-ttu-id="8a3b8-125">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="8a3b8-125">-SkuCapacity</span></span>
<span data-ttu-id="8a3b8-126">STB kapasitesi</span><span class="sxs-lookup"><span data-stu-id="8a3b8-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3b8-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8a3b8-127">-SkuName</span></span>
<span data-ttu-id="8a3b8-128">SKU adı, şimdi yalnızca ' Capacityreservatıon ' olabilir</span><span class="sxs-lookup"><span data-stu-id="8a3b8-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="8a3b8-129">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="8a3b8-129">-Tags</span></span>
<span data-ttu-id="8a3b8-130">Kümenin etiketleri</span><span class="sxs-lookup"><span data-stu-id="8a3b8-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="8a3b8-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a3b8-131">-Confirm</span></span>
<span data-ttu-id="8a3b8-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a3b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a3b8-133">-WhatIf</span></span>
<span data-ttu-id="8a3b8-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a3b8-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a3b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3b8-136">CommonParameters</span></span>
<span data-ttu-id="8a3b8-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3b8-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8a3b8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3b8-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a3b8-139">INPUTS</span></span>

### <span data-ttu-id="8a3b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8a3b8-140">System.String</span></span>

## <span data-ttu-id="8a3b8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a3b8-141">OUTPUTS</span></span>

### <span data-ttu-id="8a3b8-142">Microsoft. Azure. Commands. Operationalınsights. model. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="8a3b8-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="8a3b8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a3b8-143">NOTES</span></span>

## <span data-ttu-id="8a3b8-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a3b8-144">RELATED LINKS</span></span>
