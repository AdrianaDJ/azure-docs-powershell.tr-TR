---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105424"
---
# <span data-ttu-id="cb0c6-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cb0c6-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="cb0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0c6-103">HDInsight işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="cb0c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb0c6-104">SYNTAX</span></span>

### <span data-ttu-id="cb0c6-105">HDInsight kümesinde jobDetails 'i başlatma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb0c6-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cb0c6-106">Bir HDInsight kümesinde jobDetails 'i başlatma (belirli abonelik kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="cb0c6-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb0c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb0c6-107">DESCRIPTION</span></span>
<span data-ttu-id="cb0c6-108">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="cb0c6-109">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="cb0c6-110">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="cb0c6-111">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="cb0c6-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="cb0c6-112">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="cb0c6-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="cb0c6-113">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb0c6-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="cb0c6-114">**Start-AzureHDInsightJob** cmdlet 'i belirtilen bir kümede tanımlı bir Azure HDInsight işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="cb0c6-115">Başlangıç işi, bir MapReduce işi, bir akış işi, bir kovan işi veya bir domuz işi olabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="cb0c6-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb0c6-116">EXAMPLES</span></span>

### <span data-ttu-id="cb0c6-117">Örnek 1: HDInsight işi başlatma</span><span class="sxs-lookup"><span data-stu-id="cb0c6-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="cb0c6-118">İlk komut geçerli abonelik KIMLIĞINI alır ve $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="cb0c6-119">İkinci komut $ClusterName değişkenine Cluster01 adını atar.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="cb0c6-120">Üçüncü komut, MapReduce iş tanımı oluşturmak için **New-AzureHDInsightMapReduceJobDefinition** cmdlet 'ini kullanır ve ardından $WordCountJob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="cb0c6-121">Son komutu, **AzureHDInsightJob 'ı start-** cmdlet 'ine aktarmak için $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="cb0c6-122">İş başlatıldıktan sonra, iş çıktısını almak için **Get-AzureHDInsightJobOutput** cmdlet 'ine geçirmeden önce işin tamamlanmasını bekleyen **wait-AzureHDInsightJob** cmdlet 'ine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="cb0c6-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb0c6-123">PARAMETERS</span></span>

### <span data-ttu-id="cb0c6-124">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="cb0c6-124">-Certificate</span></span>
<span data-ttu-id="cb0c6-125">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-125">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="cb0c6-126">-Küme</span><span class="sxs-lookup"><span data-stu-id="cb0c6-126">-Cluster</span></span>
<span data-ttu-id="cb0c6-127">Bir küme belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-127">Specifies a cluster.</span></span>
<span data-ttu-id="cb0c6-128">Bu cmdlet, bu parametrenin belirttiği kümede bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0c6-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="cb0c6-129">-Credential</span></span>
<span data-ttu-id="cb0c6-130">Kümeye doğrudan HTTP erişimi için küme kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="cb0c6-131">Bir kümeye erişim doğrulaması yapmak için *abonelik* parametresi yerine bu parametreyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="cb0c6-132">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="cb0c6-132">-Endpoint</span></span>
<span data-ttu-id="cb0c6-133">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="cb0c6-134">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="cb0c6-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="cb0c6-135">-HostedService</span></span>
<span data-ttu-id="cb0c6-136">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="cb0c6-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="cb0c6-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="cb0c6-138">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="cb0c6-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb0c6-139">-JobDefinition</span></span>
<span data-ttu-id="cb0c6-140">Uç nokta varsayılan değerinden farklıysa Microsoft Azure 'a bağlanırken kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0c6-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb0c6-141">-Profile</span></span>
<span data-ttu-id="cb0c6-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb0c6-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb0c6-144">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="cb0c6-144">-Subscription</span></span>
<span data-ttu-id="cb0c6-145">Aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-145">Specifies a subscription.</span></span>
<span data-ttu-id="cb0c6-146">Bu cmdlet, bu parametrenin belirttiği abonelik için bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb0c6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0c6-147">CommonParameters</span></span>
<span data-ttu-id="cb0c6-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb0c6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0c6-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0c6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0c6-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb0c6-150">INPUTS</span></span>

## <span data-ttu-id="cb0c6-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb0c6-151">OUTPUTS</span></span>

## <span data-ttu-id="cb0c6-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb0c6-152">NOTES</span></span>

## <span data-ttu-id="cb0c6-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb0c6-153">RELATED LINKS</span></span>

[<span data-ttu-id="cb0c6-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cb0c6-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="cb0c6-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="cb0c6-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="cb0c6-156">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb0c6-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="cb0c6-157">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cb0c6-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="cb0c6-158">Bekle-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cb0c6-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


