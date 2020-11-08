---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105962"
---
# <span data-ttu-id="731f3-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="731f3-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="731f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731f3-102">SYNOPSIS</span></span>
<span data-ttu-id="731f3-103">HDInsight kümesi için veri düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="731f3-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="731f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="731f3-104">SYNTAX</span></span>

### <span data-ttu-id="731f3-105">Ad içeren düğümlerde küme boyutunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="731f3-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="731f3-106">Ardışık düzene sahip düğümlerde küme boyutunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="731f3-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="731f3-107">Ada göre küme (belirli bir aboneliğin kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="731f3-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="731f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="731f3-108">DESCRIPTION</span></span>
<span data-ttu-id="731f3-109">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="731f3-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="731f3-110">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="731f3-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="731f3-111">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="731f3-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="731f3-112">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="731f3-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="731f3-113">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="731f3-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="731f3-114">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="731f3-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="731f3-115">**Set-AzureHDInsightClusterSize** cmdlet 'i, bir Azure HDInsight kümesinin veri düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="731f3-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="731f3-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="731f3-116">EXAMPLES</span></span>

## <span data-ttu-id="731f3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="731f3-117">PARAMETERS</span></span>

### <span data-ttu-id="731f3-118">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="731f3-118">-Certificate</span></span>
<span data-ttu-id="731f3-119">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-120">-Küme</span><span class="sxs-lookup"><span data-stu-id="731f3-120">-Cluster</span></span>
<span data-ttu-id="731f3-121">Yeniden boyutlandırılacağı kümeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-122">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="731f3-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="731f3-123">Küme için oluşturulacak veri düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-124">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="731f3-124">-Endpoint</span></span>
<span data-ttu-id="731f3-125">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="731f3-126">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="731f3-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="731f3-127">-Force</span></span>
<span data-ttu-id="731f3-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="731f3-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="731f3-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="731f3-130">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="731f3-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="731f3-131">-Name</span></span>
<span data-ttu-id="731f3-132">Yeniden boyutlandırılacağı HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="731f3-133">-Profile</span></span>
<span data-ttu-id="731f3-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="731f3-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="731f3-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-136">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="731f3-136">-Subscription</span></span>
<span data-ttu-id="731f3-137">Aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="731f3-137">Specifies a subscription.</span></span>
<span data-ttu-id="731f3-138">Bu cmdlet, bu parametrenin belirttiği aboneliğin küme boyutunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="731f3-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731f3-139">CommonParameters</span></span>
<span data-ttu-id="731f3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="731f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731f3-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731f3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731f3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="731f3-142">INPUTS</span></span>

## <span data-ttu-id="731f3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="731f3-143">OUTPUTS</span></span>

## <span data-ttu-id="731f3-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="731f3-144">NOTES</span></span>

## <span data-ttu-id="731f3-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="731f3-145">RELATED LINKS</span></span>

