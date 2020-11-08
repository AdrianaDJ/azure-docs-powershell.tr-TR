---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105764"
---
# <span data-ttu-id="e5049-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e5049-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="e5049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5049-102">SYNOPSIS</span></span>
<span data-ttu-id="e5049-103">HDInsight işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e5049-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="e5049-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5049-104">SYNTAX</span></span>

### <span data-ttu-id="e5049-105">HDInsight kümesinde jobDetails 'i başlatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5049-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e5049-106">Bir HDInsight kümesinde jobDetails 'i başlatma (belirli abonelik kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="e5049-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5049-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5049-107">DESCRIPTION</span></span>
<span data-ttu-id="e5049-108">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e5049-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e5049-109">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e5049-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e5049-110">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5049-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e5049-111">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e5049-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e5049-112">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e5049-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e5049-113">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e5049-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e5049-114">**Stop-AzureHDInsightJob** cmdlet 'i belirtilen kümede bir Azure HDInsight işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e5049-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="e5049-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5049-115">EXAMPLES</span></span>

## <span data-ttu-id="e5049-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5049-116">PARAMETERS</span></span>

### <span data-ttu-id="e5049-117">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="e5049-117">-Certificate</span></span>
<span data-ttu-id="e5049-118">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-118">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-119">-Küme</span><span class="sxs-lookup"><span data-stu-id="e5049-119">-Cluster</span></span>
<span data-ttu-id="e5049-120">Bir küme belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-120">Specifies a cluster.</span></span>
<span data-ttu-id="e5049-121">Bu cmdlet, bu parametrenin belirttiği kümede çalışan bir işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="e5049-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="e5049-122">-Credential</span></span>
<span data-ttu-id="e5049-123">Bir kümeye doğrudan HTTP erişimi için kullanılacak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="e5049-124">Bir kümeye erişim doğrulaması yapmak için *abonelik* parametresi yerine bu parametreyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5049-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-125">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="e5049-125">-Endpoint</span></span>
<span data-ttu-id="e5049-126">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e5049-127">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="e5049-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e5049-128">-HostedService</span></span>
<span data-ttu-id="e5049-129">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e5049-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="e5049-131">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5049-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="e5049-132">-JobId</span></span>
<span data-ttu-id="e5049-133">Durdurulacak HDInsight işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5049-134">-Profile</span></span>
<span data-ttu-id="e5049-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5049-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e5049-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5049-137">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="e5049-137">-Subscription</span></span>
<span data-ttu-id="e5049-138">Aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5049-138">Specifies a subscription.</span></span>
<span data-ttu-id="e5049-139">Bu cmdlet, bu parametrenin belirttiği abonelik için bir iş durdurur.</span><span class="sxs-lookup"><span data-stu-id="e5049-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5049-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5049-140">CommonParameters</span></span>
<span data-ttu-id="e5049-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5049-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5049-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5049-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5049-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5049-143">INPUTS</span></span>

## <span data-ttu-id="e5049-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5049-144">OUTPUTS</span></span>

## <span data-ttu-id="e5049-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5049-145">NOTES</span></span>

## <span data-ttu-id="e5049-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5049-146">RELATED LINKS</span></span>

[<span data-ttu-id="e5049-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e5049-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="e5049-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e5049-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="e5049-149">Bekle-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e5049-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


