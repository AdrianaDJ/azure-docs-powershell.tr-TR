---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268785"
---
# <span data-ttu-id="802cf-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="802cf-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="802cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802cf-102">SYNOPSIS</span></span>
<span data-ttu-id="802cf-103">Küme kaynağını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="802cf-103">Remove cluster resource.</span></span>

## <span data-ttu-id="802cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="802cf-104">SYNTAX</span></span>

### <span data-ttu-id="802cf-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="802cf-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802cf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="802cf-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802cf-107">Byıd</span><span class="sxs-lookup"><span data-stu-id="802cf-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802cf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="802cf-108">DESCRIPTION</span></span>
<span data-ttu-id="802cf-109">Kümeyi Kaldır bu, kümenin altındaki düğüm türlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="802cf-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="802cf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="802cf-110">EXAMPLES</span></span>

### <span data-ttu-id="802cf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="802cf-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="802cf-112">Kümeyi kaldır.</span><span class="sxs-lookup"><span data-stu-id="802cf-112">Remove cluster.</span></span>

### <span data-ttu-id="802cf-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="802cf-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="802cf-114">Şeridi kullanarak kümeyi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="802cf-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="802cf-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="802cf-115">PARAMETERS</span></span>

### <span data-ttu-id="802cf-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="802cf-116">-AsJob</span></span>
<span data-ttu-id="802cf-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="802cf-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="802cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802cf-118">-DefaultProfile</span></span>
<span data-ttu-id="802cf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="802cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802cf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="802cf-120">-InputObject</span></span>
<span data-ttu-id="802cf-121">Yönetilen küme kaynağı</span><span class="sxs-lookup"><span data-stu-id="802cf-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="802cf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="802cf-122">-Name</span></span>
<span data-ttu-id="802cf-123">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="802cf-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="802cf-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="802cf-124">-PassThru</span></span>
<span data-ttu-id="802cf-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="802cf-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="802cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="802cf-127">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="802cf-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="802cf-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="802cf-128">-ResourceId</span></span>
<span data-ttu-id="802cf-129">Yönetilen küme kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="802cf-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="802cf-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="802cf-130">-Confirm</span></span>
<span data-ttu-id="802cf-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="802cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802cf-132">-WhatIf</span></span>
<span data-ttu-id="802cf-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="802cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="802cf-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="802cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="802cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802cf-135">CommonParameters</span></span>
<span data-ttu-id="802cf-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="802cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802cf-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="802cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802cf-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="802cf-138">INPUTS</span></span>

### <span data-ttu-id="802cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="802cf-139">System.String</span></span>

## <span data-ttu-id="802cf-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="802cf-140">OUTPUTS</span></span>

### <span data-ttu-id="802cf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="802cf-141">System.Boolean</span></span>

## <span data-ttu-id="802cf-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="802cf-142">NOTES</span></span>

## <span data-ttu-id="802cf-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="802cf-143">RELATED LINKS</span></span>
