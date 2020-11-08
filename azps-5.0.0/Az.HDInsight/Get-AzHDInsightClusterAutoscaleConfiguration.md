---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275375"
---
# <span data-ttu-id="24ff3-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24ff3-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="24ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="24ff3-103">HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="24ff3-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="24ff3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24ff3-104">SYNTAX</span></span>

### <span data-ttu-id="24ff3-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24ff3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24ff3-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="24ff3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24ff3-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ff3-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ff3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="24ff3-108">DESCRIPTION</span></span>
<span data-ttu-id="24ff3-109">**Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet 'i HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="24ff3-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="24ff3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="24ff3-111">Örnek 1: HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını alma.</span><span class="sxs-lookup"><span data-stu-id="24ff3-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="24ff3-112">Bu komut HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="24ff3-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="24ff3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24ff3-113">PARAMETERS</span></span>

### <span data-ttu-id="24ff3-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="24ff3-114">-ClusterName</span></span>
<span data-ttu-id="24ff3-115">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24ff3-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ff3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ff3-116">-DefaultProfile</span></span>
<span data-ttu-id="24ff3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24ff3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ff3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24ff3-118">-InputObject</span></span>
<span data-ttu-id="24ff3-119">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24ff3-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24ff3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ff3-120">-ResourceGroupName</span></span>
<span data-ttu-id="24ff3-121">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24ff3-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ff3-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="24ff3-122">-ResourceId</span></span>
<span data-ttu-id="24ff3-123">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24ff3-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ff3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ff3-124">CommonParameters</span></span>
<span data-ttu-id="24ff3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24ff3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ff3-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="24ff3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ff3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24ff3-127">INPUTS</span></span>

### <span data-ttu-id="24ff3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="24ff3-128">System.String</span></span>

### <span data-ttu-id="24ff3-129">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="24ff3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="24ff3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24ff3-130">OUTPUTS</span></span>

### <span data-ttu-id="24ff3-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="24ff3-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="24ff3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24ff3-132">NOTES</span></span>

## <span data-ttu-id="24ff3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24ff3-133">RELATED LINKS</span></span>

<span data-ttu-id="24ff3-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="24ff3-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
