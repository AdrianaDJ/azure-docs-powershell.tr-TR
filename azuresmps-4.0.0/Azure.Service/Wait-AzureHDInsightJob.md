---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105832"
---
# <span data-ttu-id="d8510-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d8510-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="d8510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8510-102">SYNOPSIS</span></span>
<span data-ttu-id="d8510-103">Bir HDInsight işinin tamamlanmasını veya başarısızlığını bekler ve işin ilerlemesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d8510-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="d8510-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8510-104">SYNTAX</span></span>

### <span data-ttu-id="d8510-105">HDInsight kümesinin jobDetails geçmişini alma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8510-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8510-106">HDInsight kümesinin jobDetails geçmişini alma (belirli bir aboneliğin kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="d8510-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8510-107">HDInsight kümesinde JobId ile bekleme Işi</span><span class="sxs-lookup"><span data-stu-id="d8510-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8510-108">HDInsight kümesinde Iş ile işi bekleme Işi</span><span class="sxs-lookup"><span data-stu-id="d8510-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8510-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8510-109">DESCRIPTION</span></span>
<span data-ttu-id="d8510-110">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="d8510-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d8510-111">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d8510-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d8510-112">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8510-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d8510-113">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d8510-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d8510-114">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d8510-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d8510-115">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d8510-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d8510-116">**Wait-AzureHDInsightJob** cmdlet 'ı bir Azure HDInsight işinin tamamlanması veya başarısızlığını bekler ve işin ilerlemesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d8510-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="d8510-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8510-117">EXAMPLES</span></span>

### <span data-ttu-id="d8510-118">Örnek 1: bir iş çalıştırıp tamamlamasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="d8510-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="d8510-119">İlk komut geçerli Azure aboneliği KIMLIĞINI alır ve $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8510-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="d8510-120">İkinci komut belirtilen kümeyi alır ve $ClusterName değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8510-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="d8510-121">Üçüncü komut, MapReduce iş tanımı oluşturmak için **New-AzureHDInsightMapReduceJobDefinition** cmdlet 'ini kullanır ve ardından $WordCountJob değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8510-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="d8510-122">Dördüncü komut sırayla birkaç cmdlet kullanır:</span><span class="sxs-lookup"><span data-stu-id="d8510-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="d8510-123">**Başlangıç-AzureHDInsightJob** cmdlet 'ine $WordCountJob geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d8510-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="d8510-124">İş, işin tamamlanması için 3600 saniye beklemek için **wait-AzureHDInsightJob** cmdlet 'ine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="d8510-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="d8510-125">İş tamamlandığında, komut **Get-AzureHDInsightJobOutput** cmdlet 'ini kullanarak iş çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="d8510-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="d8510-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8510-126">PARAMETERS</span></span>

### <span data-ttu-id="d8510-127">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="d8510-127">-Certificate</span></span>
<span data-ttu-id="d8510-128">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-129">-Küme</span><span class="sxs-lookup"><span data-stu-id="d8510-129">-Cluster</span></span>
<span data-ttu-id="d8510-130">Bir küme belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-130">Specifies a cluster.</span></span>
<span data-ttu-id="d8510-131">Bu cmdlet kümede bu parametrenin belirttiği işi bekler.</span><span class="sxs-lookup"><span data-stu-id="d8510-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="d8510-132">-Credential</span></span>
<span data-ttu-id="d8510-133">Bir kümeye doğrudan HTTP erişimi için kullanılacak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="d8510-134">Bir kümeye erişim doğrulaması yapmak için *abonelik* parametresi yerine bu parametreyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8510-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-135">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="d8510-135">-Endpoint</span></span>
<span data-ttu-id="d8510-136">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="d8510-137">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="d8510-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="d8510-138">-HostedService</span></span>
<span data-ttu-id="d8510-139">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="d8510-140">Bu parametreyi belirtmezseniz, varsayılan ad alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8510-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="d8510-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="d8510-142">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8510-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-143">-Job</span><span class="sxs-lookup"><span data-stu-id="d8510-143">-Job</span></span>
<span data-ttu-id="d8510-144">Bir Azure HDInsight işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="d8510-145">-JobId</span></span>
<span data-ttu-id="d8510-146">Bekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8510-147">-Profile</span></span>
<span data-ttu-id="d8510-148">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8510-149">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d8510-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8510-150">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="d8510-150">-Subscription</span></span>
<span data-ttu-id="d8510-151">Aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-151">Specifies a subscription.</span></span>
<span data-ttu-id="d8510-152">Bu cmdlet, bu parametrenin belirttiği abonelik için bir iş bekler.</span><span class="sxs-lookup"><span data-stu-id="d8510-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-153">-Waittimeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="d8510-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="d8510-154">Bekleme işlemi için zaman aşımını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8510-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="d8510-155">Zaman aşımı iş tamamlanmadan önce dolarsa, cmdlet çalışmaya sona erer.</span><span class="sxs-lookup"><span data-stu-id="d8510-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8510-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8510-156">CommonParameters</span></span>
<span data-ttu-id="d8510-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8510-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8510-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8510-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8510-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8510-159">INPUTS</span></span>

## <span data-ttu-id="d8510-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8510-160">OUTPUTS</span></span>

## <span data-ttu-id="d8510-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8510-161">NOTES</span></span>

## <span data-ttu-id="d8510-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8510-162">RELATED LINKS</span></span>

[<span data-ttu-id="d8510-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d8510-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="d8510-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="d8510-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="d8510-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d8510-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="d8510-166">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d8510-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


