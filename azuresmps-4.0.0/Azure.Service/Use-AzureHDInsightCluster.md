---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105837"
---
# <span data-ttu-id="8d126-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8d126-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="8d126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d126-102">SYNOPSIS</span></span>
<span data-ttu-id="8d126-103">Invoke-AzureHDInsightHiveJob cmdlet 'i, işleri göndermek için kullanılacak bir HDInsight kümesi seçer.</span><span class="sxs-lookup"><span data-stu-id="8d126-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="8d126-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d126-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d126-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d126-105">DESCRIPTION</span></span>
<span data-ttu-id="8d126-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="8d126-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8d126-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="8d126-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8d126-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d126-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8d126-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8d126-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8d126-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8d126-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8d126-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8d126-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8d126-112">**Use-AzureHDInsightCluster** cmdlet 'i, iş göndermek Için kullanılacak **Invoke-AzureHDInsightHiveJob** cmdlet 'inin Azure HDInsight kümesini seçer.</span><span class="sxs-lookup"><span data-stu-id="8d126-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="8d126-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d126-113">EXAMPLES</span></span>

## <span data-ttu-id="8d126-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d126-114">PARAMETERS</span></span>

### <span data-ttu-id="8d126-115">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="8d126-115">-Certificate</span></span>
<span data-ttu-id="8d126-116">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="8d126-117">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="8d126-117">-Endpoint</span></span>
<span data-ttu-id="8d126-118">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="8d126-119">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="8d126-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="8d126-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="8d126-120">-HostedService</span></span>
<span data-ttu-id="8d126-121">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="8d126-122">Bu parametreyi belirtmezseniz, varsayılan ad alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d126-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="8d126-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="8d126-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="8d126-124">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d126-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="8d126-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d126-125">-Name</span></span>
<span data-ttu-id="8d126-126">**Invoke-AzureHDInsightHiveJob** cmdlet 'i tarafından kullanılan kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="8d126-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d126-127">-Profile</span></span>
<span data-ttu-id="8d126-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d126-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8d126-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d126-130">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="8d126-130">-Subscription</span></span>
<span data-ttu-id="8d126-131">Kullanılacak HDInsight kümelerini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d126-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="8d126-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d126-132">CommonParameters</span></span>
<span data-ttu-id="8d126-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d126-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d126-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d126-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d126-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d126-135">INPUTS</span></span>

## <span data-ttu-id="8d126-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d126-136">OUTPUTS</span></span>

## <span data-ttu-id="8d126-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d126-137">NOTES</span></span>

## <span data-ttu-id="8d126-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d126-138">RELATED LINKS</span></span>

[<span data-ttu-id="8d126-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8d126-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="8d126-140">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8d126-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="8d126-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8d126-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


