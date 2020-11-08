---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278678"
---
# <span data-ttu-id="b6f25-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b6f25-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="b6f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f25-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f25-103">Yeni adanmış bir eventhub kümesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b6f25-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="b6f25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6f25-104">SYNTAX</span></span>

### <span data-ttu-id="b6f25-105">ClusterPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6f25-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6f25-106">Clusterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b6f25-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f25-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6f25-107">DESCRIPTION</span></span>
<span data-ttu-id="b6f25-108">New-AzEventHubCluster cmdlet 'i, verilen kaynak grubunda adanmış eventhub kümesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b6f25-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="b6f25-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6f25-109">EXAMPLES</span></span>

### <span data-ttu-id="b6f25-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6f25-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="b6f25-111">' RSG-Cluster27651 ' için resourcegroup ', ' Eventhub-Cluster-5557 ' ile</span><span class="sxs-lookup"><span data-stu-id="b6f25-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="b6f25-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6f25-112">PARAMETERS</span></span>

### <span data-ttu-id="b6f25-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="b6f25-113">-Capacity</span></span>
<span data-ttu-id="b6f25-114">Küme kapasitesi (CU), curerntrly, izin verilen değer = 1</span><span class="sxs-lookup"><span data-stu-id="b6f25-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f25-115">-DefaultProfile</span></span>
<span data-ttu-id="b6f25-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6f25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b6f25-117">-Location</span></span>
<span data-ttu-id="b6f25-118">Kümenin konumu</span><span class="sxs-lookup"><span data-stu-id="b6f25-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6f25-119">-Name</span></span>
<span data-ttu-id="b6f25-120">Küme adı</span><span class="sxs-lookup"><span data-stu-id="b6f25-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f25-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6f25-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b6f25-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6f25-123">-ResourceId</span></span>
<span data-ttu-id="b6f25-124">Kümenin kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="b6f25-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6f25-125">-Tag</span></span>
<span data-ttu-id="b6f25-126">Kümeler için kaynak etiketlerini temsil eden hashtables</span><span class="sxs-lookup"><span data-stu-id="b6f25-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f25-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6f25-127">-Confirm</span></span>
<span data-ttu-id="b6f25-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6f25-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f25-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f25-129">-WhatIf</span></span>
<span data-ttu-id="b6f25-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6f25-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f25-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6f25-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f25-132">CommonParameters</span></span>
<span data-ttu-id="b6f25-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6f25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f25-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6f25-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f25-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6f25-135">INPUTS</span></span>

### <span data-ttu-id="b6f25-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f25-136">System.String</span></span>

### <span data-ttu-id="b6f25-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b6f25-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b6f25-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6f25-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6f25-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6f25-139">OUTPUTS</span></span>

### <span data-ttu-id="b6f25-140">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubclusterattributes</span><span class="sxs-lookup"><span data-stu-id="b6f25-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="b6f25-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6f25-141">NOTES</span></span>

## <span data-ttu-id="b6f25-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6f25-142">RELATED LINKS</span></span>
