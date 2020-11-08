---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267624"
---
# <span data-ttu-id="b06df-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b06df-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="b06df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b06df-102">SYNOPSIS</span></span>
<span data-ttu-id="b06df-103">Düğüm türünden belirli düğümleri yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="b06df-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="b06df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b06df-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b06df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b06df-105">DESCRIPTION</span></span>
<span data-ttu-id="b06df-106">Düğüm türünden belirli düğümleri yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="b06df-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="b06df-107">Hizmet yapısı düğümlerini, VM 'leri yeniden başlatmadan önce devre dışı bırakmış ve geri geldikten sonra tekrar etkinleştirmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="b06df-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="b06df-108">Bu, birincil düğüm türlerinde yapıldığında, aynı anda tüm düğümleri yeniden başlatmayabilir.</span><span class="sxs-lookup"><span data-stu-id="b06df-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="b06df-109">Use-ForceRestart işlemi, hizmet yapısı düğümleri devre dışı bırakmasa da işlemi zorunlu tutar, ancak bu işlem sonucunda durum bilgisi olan iş yükleri çalışırken veri kaybına neden olabileceğinden dikkatli kullanın.</span><span class="sxs-lookup"><span data-stu-id="b06df-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="b06df-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b06df-110">EXAMPLES</span></span>

### <span data-ttu-id="b06df-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b06df-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="b06df-112">Düğüm türünde 0 ve 3 düğümünü yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="b06df-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="b06df-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b06df-113">PARAMETERS</span></span>

### <span data-ttu-id="b06df-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b06df-114">-AsJob</span></span>
<span data-ttu-id="b06df-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b06df-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b06df-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b06df-116">-ClusterName</span></span>
<span data-ttu-id="b06df-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b06df-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b06df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06df-118">-DefaultProfile</span></span>
<span data-ttu-id="b06df-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b06df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06df-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="b06df-120">-ForceRestart</span></span>
<span data-ttu-id="b06df-121">Bu bayrak kullanıldığında, hizmet yapısı düğümleri devre dışı bırakmasa bile düğüm yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="b06df-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="b06df-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b06df-122">-Name</span></span>
<span data-ttu-id="b06df-123">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b06df-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06df-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="b06df-124">-NodeName</span></span>
<span data-ttu-id="b06df-125">İşlemin düğüm adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="b06df-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06df-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b06df-126">-PassThru</span></span>
<span data-ttu-id="b06df-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b06df-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b06df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06df-128">-ResourceGroupName</span></span>
<span data-ttu-id="b06df-129">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b06df-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06df-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b06df-130">-Confirm</span></span>
<span data-ttu-id="b06df-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b06df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b06df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b06df-132">-WhatIf</span></span>
<span data-ttu-id="b06df-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b06df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b06df-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b06df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b06df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06df-135">CommonParameters</span></span>
<span data-ttu-id="b06df-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b06df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06df-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b06df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06df-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b06df-138">INPUTS</span></span>

### <span data-ttu-id="b06df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b06df-139">System.String</span></span>

## <span data-ttu-id="b06df-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b06df-140">OUTPUTS</span></span>

### <span data-ttu-id="b06df-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b06df-141">System.Boolean</span></span>

## <span data-ttu-id="b06df-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b06df-142">NOTES</span></span>

## <span data-ttu-id="b06df-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b06df-143">RELATED LINKS</span></span>
