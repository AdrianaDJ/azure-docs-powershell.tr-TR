---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109631"
---
# <span data-ttu-id="81f57-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="81f57-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="81f57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f57-102">SYNOPSIS</span></span>
<span data-ttu-id="81f57-103">HDInsight kümesinin belirli konaklarını yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="81f57-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="81f57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81f57-104">SYNTAX</span></span>

### <span data-ttu-id="81f57-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81f57-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f57-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f57-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f57-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81f57-107">DESCRIPTION</span></span>
<span data-ttu-id="81f57-108">Bu **restart-AzHDInsightHost** cmdlet 'i HDInsight kümesinin belirli konaklarını yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="81f57-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="81f57-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81f57-109">EXAMPLES</span></span>

### <span data-ttu-id="81f57-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="81f57-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="81f57-111">Bu komut, kümenin iki ana bilgisayarını yeniden başlatır: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="81f57-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="81f57-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="81f57-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="81f57-113">Bu komut, ' Get-AzHDInsightHost ' cmdlet 'ine birlikte çalışmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="81f57-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="81f57-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81f57-114">PARAMETERS</span></span>

### <span data-ttu-id="81f57-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="81f57-115">-AsJob</span></span>
<span data-ttu-id="81f57-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="81f57-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81f57-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="81f57-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="81f57-118">Konağın adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81f57-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f57-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="81f57-119">-ClusterName</span></span>
<span data-ttu-id="81f57-120">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81f57-120">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f57-121">-DefaultProfile</span></span>
<span data-ttu-id="81f57-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81f57-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f57-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="81f57-123">-Name</span></span>
<span data-ttu-id="81f57-124">Konağın adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81f57-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f57-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="81f57-125">-PassThru</span></span>
<span data-ttu-id="81f57-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="81f57-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="81f57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f57-127">-ResourceGroupName</span></span>
<span data-ttu-id="81f57-128">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81f57-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f57-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="81f57-129">-Confirm</span></span>
<span data-ttu-id="81f57-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81f57-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f57-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f57-131">-WhatIf</span></span>
<span data-ttu-id="81f57-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81f57-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81f57-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81f57-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f57-134">CommonParameters</span></span>
<span data-ttu-id="81f57-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81f57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f57-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="81f57-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f57-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81f57-137">INPUTS</span></span>

### <span data-ttu-id="81f57-138">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. HDInsight. modeller. Management. AzureHDInsightHostInfo, Microsoft. Azure. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81f57-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81f57-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81f57-139">OUTPUTS</span></span>

### <span data-ttu-id="81f57-140">Microsoft. Azure. Management. HDInsight. modeller. Cluster</span><span class="sxs-lookup"><span data-stu-id="81f57-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="81f57-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81f57-141">NOTES</span></span>

## <span data-ttu-id="81f57-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81f57-142">RELATED LINKS</span></span>
