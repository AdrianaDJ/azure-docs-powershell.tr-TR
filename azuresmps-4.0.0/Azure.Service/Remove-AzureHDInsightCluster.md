---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106476"
---
# <span data-ttu-id="e2891-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2891-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="e2891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2891-102">SYNOPSIS</span></span>
<span data-ttu-id="e2891-103">Bir aboneliğindeki HDInsight kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="e2891-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="e2891-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2891-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2891-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2891-105">DESCRIPTION</span></span>
<span data-ttu-id="e2891-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e2891-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e2891-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e2891-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e2891-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="e2891-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e2891-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e2891-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e2891-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e2891-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e2891-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e2891-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e2891-112">**Remove-AzureHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten siler.</span><span class="sxs-lookup"><span data-stu-id="e2891-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="e2891-113">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="e2891-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="e2891-114">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="e2891-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="e2891-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2891-115">EXAMPLES</span></span>

### <span data-ttu-id="e2891-116">Örnek 1: kümeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="e2891-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="e2891-117">Bu komut, HDICluster adlı HDInsight kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="e2891-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="e2891-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2891-118">PARAMETERS</span></span>

### <span data-ttu-id="e2891-119">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="e2891-119">-Certificate</span></span>
<span data-ttu-id="e2891-120">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-120">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-121">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="e2891-121">-Endpoint</span></span>
<span data-ttu-id="e2891-122">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e2891-123">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2891-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e2891-124">-HostedService</span></span>
<span data-ttu-id="e2891-125">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e2891-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="e2891-127">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2891-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2891-128">-Name</span></span>
<span data-ttu-id="e2891-129">Kaldırılacak HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-129">Specifies the name of the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2891-130">-Profile</span></span>
<span data-ttu-id="e2891-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2891-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2891-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2891-133">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="e2891-133">-Subscription</span></span>
<span data-ttu-id="e2891-134">Kaldırılacak HDInsight kümesini içeren abonelik hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2891-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2891-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2891-135">CommonParameters</span></span>
<span data-ttu-id="e2891-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2891-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2891-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2891-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2891-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2891-138">INPUTS</span></span>

## <span data-ttu-id="e2891-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2891-139">OUTPUTS</span></span>

## <span data-ttu-id="e2891-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2891-140">NOTES</span></span>

## <span data-ttu-id="e2891-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2891-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2891-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2891-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="e2891-143">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2891-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e2891-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2891-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


