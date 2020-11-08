---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275458"
---
# <span data-ttu-id="0c238-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="0c238-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="0c238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c238-102">SYNOPSIS</span></span>
<span data-ttu-id="0c238-103">Belirtilen adanmış Eventhub kümesini ResourceGroup 'i veritabanından siler</span><span class="sxs-lookup"><span data-stu-id="0c238-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="0c238-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c238-104">SYNTAX</span></span>

### <span data-ttu-id="0c238-105">ClusterPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c238-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c238-106">Clusterınputobjectset</span><span class="sxs-lookup"><span data-stu-id="0c238-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c238-107">Clusterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0c238-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c238-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c238-108">DESCRIPTION</span></span>
<span data-ttu-id="0c238-109">Remove-AzEventHubCluster cmdlet 'i verili bir resourcegroup</span><span class="sxs-lookup"><span data-stu-id="0c238-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="0c238-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c238-110">EXAMPLES</span></span>

### <span data-ttu-id="0c238-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c238-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="0c238-112">RSG-Cluster27651 resourcegroup 'den Eventhub-Cluster-5557 kümesini silme</span><span class="sxs-lookup"><span data-stu-id="0c238-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="0c238-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c238-113">PARAMETERS</span></span>

### <span data-ttu-id="0c238-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c238-114">-AsJob</span></span>
<span data-ttu-id="0c238-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0c238-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c238-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c238-116">-DefaultProfile</span></span>
<span data-ttu-id="0c238-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c238-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c238-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c238-118">-InputObject</span></span>
<span data-ttu-id="0c238-119">Cluster nesnesi</span><span class="sxs-lookup"><span data-stu-id="0c238-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c238-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c238-120">-Name</span></span>
<span data-ttu-id="0c238-121">Küme adı</span><span class="sxs-lookup"><span data-stu-id="0c238-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c238-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0c238-122">-PassThru</span></span>
<span data-ttu-id="0c238-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0c238-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c238-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c238-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c238-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0c238-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0c238-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c238-126">-ResourceId</span></span>
<span data-ttu-id="0c238-127">Küme kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="0c238-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c238-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c238-128">-Confirm</span></span>
<span data-ttu-id="0c238-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c238-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c238-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c238-130">-WhatIf</span></span>
<span data-ttu-id="0c238-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c238-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c238-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c238-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c238-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c238-133">CommonParameters</span></span>
<span data-ttu-id="0c238-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c238-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c238-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c238-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c238-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c238-136">INPUTS</span></span>

### <span data-ttu-id="0c238-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0c238-137">System.String</span></span>

### <span data-ttu-id="0c238-138">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="0c238-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="0c238-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c238-139">OUTPUTS</span></span>

### <span data-ttu-id="0c238-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c238-140">System.Boolean</span></span>

## <span data-ttu-id="0c238-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c238-141">NOTES</span></span>

## <span data-ttu-id="0c238-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c238-142">RELATED LINKS</span></span>
