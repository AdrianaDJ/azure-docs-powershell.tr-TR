---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105644"
---
# <span data-ttu-id="13a3f-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="13a3f-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="13a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="13a3f-103">HDInsight kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="13a3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13a3f-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="13a3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="13a3f-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="13a3f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="13a3f-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="13a3f-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="13a3f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="13a3f-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="13a3f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="13a3f-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="13a3f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="13a3f-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="13a3f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="13a3f-112">**Get-AzureHDInsightCluster** cmdlet 'i geçerli aboneliğin Azure HDInsight hizmet kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="13a3f-113">Belirli bir kümeyi almak için *Name* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13a3f-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="13a3f-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13a3f-114">EXAMPLES</span></span>

### <span data-ttu-id="13a3f-115">Örnek 1: bir abonelikteki kümeleri alma</span><span class="sxs-lookup"><span data-stu-id="13a3f-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="13a3f-116">Bu komut, geçerli abonelikteki HDInsight kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="13a3f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13a3f-117">PARAMETERS</span></span>

### <span data-ttu-id="13a3f-118">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="13a3f-118">-Certificate</span></span>
<span data-ttu-id="13a3f-119">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="13a3f-120">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="13a3f-120">-Endpoint</span></span>
<span data-ttu-id="13a3f-121">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="13a3f-122">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="13a3f-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="13a3f-123">-HostedService</span></span>
<span data-ttu-id="13a3f-124">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="13a3f-125">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="13a3f-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="13a3f-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="13a3f-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="13a3f-127">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="13a3f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="13a3f-128">-Name</span></span>
<span data-ttu-id="13a3f-129">Alınacak bir HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13a3f-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="13a3f-130">-Profile</span></span>
<span data-ttu-id="13a3f-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13a3f-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="13a3f-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13a3f-133">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="13a3f-133">-Subscription</span></span>
<span data-ttu-id="13a3f-134">Alınacak HDInsight kümesini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="13a3f-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="13a3f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a3f-135">CommonParameters</span></span>
<span data-ttu-id="13a3f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13a3f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a3f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a3f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a3f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13a3f-138">INPUTS</span></span>

## <span data-ttu-id="13a3f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13a3f-139">OUTPUTS</span></span>

## <span data-ttu-id="13a3f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13a3f-140">NOTES</span></span>

## <span data-ttu-id="13a3f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13a3f-141">RELATED LINKS</span></span>

[<span data-ttu-id="13a3f-142">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="13a3f-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="13a3f-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="13a3f-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="13a3f-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="13a3f-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


