---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322567"
---
# <span data-ttu-id="5f4ee-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5f4ee-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="5f4ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4ee-103">Özel bulutta küme oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f4ee-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5f4ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f4ee-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f4ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5f4ee-106">Özel bulutta küme oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f4ee-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5f4ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f4ee-107">EXAMPLES</span></span>

### <span data-ttu-id="5f4ee-108">Örnek 1: küme oluşturma</span><span class="sxs-lookup"><span data-stu-id="5f4ee-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5f4ee-109">Küme Oluştur</span><span class="sxs-lookup"><span data-stu-id="5f4ee-109">Create cluster</span></span>

## <span data-ttu-id="5f4ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f4ee-110">PARAMETERS</span></span>

### <span data-ttu-id="5f4ee-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5f4ee-111">-AsJob</span></span>
<span data-ttu-id="5f4ee-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5f4ee-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5f4ee-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="5f4ee-113">-ClusterSize</span></span>
<span data-ttu-id="5f4ee-114">Küme boyutu</span><span class="sxs-lookup"><span data-stu-id="5f4ee-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4ee-115">-DefaultProfile</span></span>
<span data-ttu-id="5f4ee-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f4ee-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f4ee-117">-Name</span></span>
<span data-ttu-id="5f4ee-118">Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="5f4ee-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4ee-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5f4ee-119">-NoWait</span></span>
<span data-ttu-id="5f4ee-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5f4ee-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5f4ee-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5f4ee-121">-PrivateCloudName</span></span>
<span data-ttu-id="5f4ee-122">Özel bulutun adı.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="5f4ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f4ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f4ee-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-124">The name of the resource group.</span></span>
<span data-ttu-id="5f4ee-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f4ee-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5f4ee-126">-SkuName</span></span>
<span data-ttu-id="5f4ee-127">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="5f4ee-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5f4ee-128">-SubscriptionId</span></span>
<span data-ttu-id="5f4ee-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4ee-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f4ee-130">-Confirm</span></span>
<span data-ttu-id="5f4ee-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f4ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f4ee-132">-WhatIf</span></span>
<span data-ttu-id="5f4ee-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f4ee-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f4ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4ee-135">CommonParameters</span></span>
<span data-ttu-id="5f4ee-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4ee-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f4ee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4ee-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f4ee-138">INPUTS</span></span>

## <span data-ttu-id="5f4ee-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f4ee-139">OUTPUTS</span></span>

### <span data-ttu-id="5f4ee-140">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıluster</span><span class="sxs-lookup"><span data-stu-id="5f4ee-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5f4ee-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f4ee-141">NOTES</span></span>

<span data-ttu-id="5f4ee-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5f4ee-142">ALIASES</span></span>

## <span data-ttu-id="5f4ee-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f4ee-143">RELATED LINKS</span></span>

