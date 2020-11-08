---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 5f5c8c193a352738f64d595188247bf0564bea43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109619"
---
# <span data-ttu-id="96399-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="96399-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="96399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96399-102">SYNOPSIS</span></span>
<span data-ttu-id="96399-103">Azure HDInsight kümesinin ağ geçidi HTTP kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="96399-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96399-104">SYNTAX</span></span>

### <span data-ttu-id="96399-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96399-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96399-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96399-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96399-107">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="96399-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96399-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="96399-108">DESCRIPTION</span></span>
<span data-ttu-id="96399-109">**Set-AzHDInsightGatewayCredential** cmdlet 'ı bir Azure HDInsight kümesinin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="96399-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96399-110">EXAMPLES</span></span>

### <span data-ttu-id="96399-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96399-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="96399-112">Bu komut,-Hadoop-001 ad parametresi kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="96399-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="96399-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="96399-114">Bu komut,-Hadoop-001 ile RESOURCEID parametre kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="96399-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="96399-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="96399-116">Bu komut,-Hadoop-001 ile InputObject parametre kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="96399-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96399-117">PARAMETERS</span></span>

### <span data-ttu-id="96399-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="96399-118">-AsJob</span></span>
<span data-ttu-id="96399-119">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="96399-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="96399-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96399-120">-DefaultProfile</span></span>
<span data-ttu-id="96399-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96399-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96399-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="96399-122">-HttpCredential</span></span>
<span data-ttu-id="96399-123">Kümenin kullanıcısı için oturum açmayı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96399-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96399-124">-InputObject</span></span>
<span data-ttu-id="96399-125">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96399-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="96399-126">-Name</span></span>
<span data-ttu-id="96399-127">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96399-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96399-128">-ResourceGroupName</span></span>
<span data-ttu-id="96399-129">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="96399-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="96399-130">-ResourceId</span></span>
<span data-ttu-id="96399-131">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="96399-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96399-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="96399-132">-Confirm</span></span>
<span data-ttu-id="96399-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96399-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96399-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96399-134">-WhatIf</span></span>
<span data-ttu-id="96399-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96399-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96399-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96399-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96399-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96399-137">CommonParameters</span></span>
<span data-ttu-id="96399-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96399-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96399-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="96399-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96399-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96399-140">INPUTS</span></span>

### <span data-ttu-id="96399-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96399-141">None</span></span>

## <span data-ttu-id="96399-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96399-142">OUTPUTS</span></span>

### <span data-ttu-id="96399-143">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="96399-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="96399-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96399-144">NOTES</span></span>

## <span data-ttu-id="96399-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96399-145">RELATED LINKS</span></span>
