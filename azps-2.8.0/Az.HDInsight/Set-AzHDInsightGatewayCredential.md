---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 045b0db296a9c3bde4332ce755c055d1e8616738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751809"
---
# <span data-ttu-id="c70d0-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="c70d0-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="c70d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c70d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c70d0-103">Azure HDInsight kümesinin ağ geçidi HTTP kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c70d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c70d0-104">SYNTAX</span></span>

### <span data-ttu-id="c70d0-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c70d0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c70d0-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c70d0-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c70d0-107">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c70d0-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c70d0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c70d0-108">DESCRIPTION</span></span>
<span data-ttu-id="c70d0-109">**Set-AzHDInsightGatewayCredential** cmdlet 'ı bir Azure HDInsight kümesinin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c70d0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c70d0-110">EXAMPLES</span></span>

### <span data-ttu-id="c70d0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c70d0-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="c70d0-112">Bu komut,-Hadoop-001 ad parametresi kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="c70d0-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c70d0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="c70d0-114">Bu komut,-Hadoop-001 ile RESOURCEID parametre kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="c70d0-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c70d0-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="c70d0-116">Bu komut,-Hadoop-001 ile InputObject parametre kümesi adlı kümenin Ağ Geçidi kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="c70d0-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c70d0-117">PARAMETERS</span></span>

### <span data-ttu-id="c70d0-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="c70d0-118">-AsJob</span></span>
<span data-ttu-id="c70d0-119">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="c70d0-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c70d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70d0-120">-DefaultProfile</span></span>
<span data-ttu-id="c70d0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c70d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c70d0-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c70d0-122">-HttpCredential</span></span>
<span data-ttu-id="c70d0-123">Kümenin kullanıcısı için oturum açmayı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="c70d0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c70d0-124">-InputObject</span></span>
<span data-ttu-id="c70d0-125">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="c70d0-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c70d0-126">-Name</span></span>
<span data-ttu-id="c70d0-127">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-127">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="c70d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c70d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="c70d0-129">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="c70d0-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c70d0-130">-ResourceId</span></span>
<span data-ttu-id="c70d0-131">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c70d0-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="c70d0-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c70d0-132">-Confirm</span></span>
<span data-ttu-id="c70d0-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c70d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c70d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c70d0-134">-WhatIf</span></span>
<span data-ttu-id="c70d0-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c70d0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c70d0-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c70d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c70d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70d0-137">CommonParameters</span></span>
<span data-ttu-id="c70d0-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c70d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70d0-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c70d0-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70d0-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c70d0-140">INPUTS</span></span>

### <span data-ttu-id="c70d0-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c70d0-141">None</span></span>

## <span data-ttu-id="c70d0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c70d0-142">OUTPUTS</span></span>

### <span data-ttu-id="c70d0-143">Microsoft. Azure. Management. HDInsight. model. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="c70d0-143">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="c70d0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c70d0-144">NOTES</span></span>

## <span data-ttu-id="c70d0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c70d0-145">RELATED LINKS</span></span>
