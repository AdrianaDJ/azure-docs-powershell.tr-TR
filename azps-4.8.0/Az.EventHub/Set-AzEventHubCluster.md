---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268255"
---
# <span data-ttu-id="7ca8d-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="7ca8d-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="7ca8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca8d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca8d-103">Verilen kümenin etiketini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7ca8d-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="7ca8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ca8d-104">SYNTAX</span></span>

### <span data-ttu-id="7ca8d-105">ClusterPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ca8d-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca8d-106">Clusterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7ca8d-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca8d-107">Clusterınputobjectset</span><span class="sxs-lookup"><span data-stu-id="7ca8d-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca8d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ca8d-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca8d-109">Set-AzEventHubCluster cmdlet, verilen kümenin etiketlerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7ca8d-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="7ca8d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ca8d-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca8d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ca8d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="7ca8d-112">Verilen kümenin etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="7ca8d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ca8d-113">PARAMETERS</span></span>

### <span data-ttu-id="7ca8d-114">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="7ca8d-114">-Capacity</span></span>
<span data-ttu-id="7ca8d-115">Küme kapasitesi (CU), curerntrly, izin verilen değer = 1</span><span class="sxs-lookup"><span data-stu-id="7ca8d-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="7ca8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca8d-116">-DefaultProfile</span></span>
<span data-ttu-id="7ca8d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca8d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca8d-118">-InputObject</span></span>
<span data-ttu-id="7ca8d-119">Küme adı</span><span class="sxs-lookup"><span data-stu-id="7ca8d-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca8d-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="7ca8d-120">-Location</span></span>
<span data-ttu-id="7ca8d-121">Kümenin konumu</span><span class="sxs-lookup"><span data-stu-id="7ca8d-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca8d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ca8d-122">-Name</span></span>
<span data-ttu-id="7ca8d-123">Küme adı</span><span class="sxs-lookup"><span data-stu-id="7ca8d-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ca8d-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7ca8d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7ca8d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7ca8d-126">-ResourceId</span></span>
<span data-ttu-id="7ca8d-127">Kümenin kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="7ca8d-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="7ca8d-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7ca8d-128">-Tag</span></span>
<span data-ttu-id="7ca8d-129">Kümeler için kaynak etiketini temsil eden hashtables</span><span class="sxs-lookup"><span data-stu-id="7ca8d-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca8d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ca8d-130">-Confirm</span></span>
<span data-ttu-id="7ca8d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca8d-132">-WhatIf</span></span>
<span data-ttu-id="7ca8d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca8d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca8d-135">CommonParameters</span></span>
<span data-ttu-id="7ca8d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca8d-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7ca8d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca8d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ca8d-138">INPUTS</span></span>

### <span data-ttu-id="7ca8d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca8d-139">System.String</span></span>

### <span data-ttu-id="7ca8d-140">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ca8d-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ca8d-141">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubclusterattributes</span><span class="sxs-lookup"><span data-stu-id="7ca8d-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="7ca8d-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ca8d-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ca8d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ca8d-143">OUTPUTS</span></span>

### <span data-ttu-id="7ca8d-144">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubclusterattributes</span><span class="sxs-lookup"><span data-stu-id="7ca8d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="7ca8d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ca8d-145">NOTES</span></span>

## <span data-ttu-id="7ca8d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ca8d-146">RELATED LINKS</span></span>
