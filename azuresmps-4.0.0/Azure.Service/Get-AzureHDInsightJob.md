---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106350"
---
# <span data-ttu-id="e0c4b-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e0c4b-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="e0c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c4b-103">HDInsight işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="e0c4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0c4b-104">SYNTAX</span></span>

### <span data-ttu-id="e0c4b-105">HDInsight kümesinin jobDetails geçmişini alma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0c4b-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0c4b-106">HDInsight kümesinin jobDetails geçmişini alma (belirli bir aboneliğin kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="e0c4b-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0c4b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0c4b-107">DESCRIPTION</span></span>
<span data-ttu-id="e0c4b-108">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e0c4b-109">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e0c4b-110">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e0c4b-111">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e0c4b-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e0c4b-112">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e0c4b-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e0c4b-113">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0c4b-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e0c4b-114">**Get-AzureHDInsightJob** cmdlet 'i belirtilen kümenin en son Azure HDInsight işlerini alır ve bunları ters sırayla görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="e0c4b-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0c4b-115">EXAMPLES</span></span>

## <span data-ttu-id="e0c4b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0c4b-116">PARAMETERS</span></span>

### <span data-ttu-id="e0c4b-117">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="e0c4b-117">-Certificate</span></span>
<span data-ttu-id="e0c4b-118">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="e0c4b-119">-Küme</span><span class="sxs-lookup"><span data-stu-id="e0c4b-119">-Cluster</span></span>
<span data-ttu-id="e0c4b-120">Bir küme belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-120">Specifies a cluster.</span></span>
<span data-ttu-id="e0c4b-121">Bu cmdlet, bu parametrenin belirttiği kümede çalışan HDInsight işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c4b-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="e0c4b-122">-Credential</span></span>
<span data-ttu-id="e0c4b-123">Bir kümeye doğrudan HTTP erişimi için kullanılacak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="e0c4b-124">Bir kümeye erişim doğrulaması yapmak için *abonelik* parametresi yerine bu parametreyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c4b-125">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="e0c4b-125">-Endpoint</span></span>
<span data-ttu-id="e0c4b-126">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e0c4b-127">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="e0c4b-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e0c4b-128">-HostedService</span></span>
<span data-ttu-id="e0c4b-129">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="e0c4b-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e0c4b-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="e0c4b-131">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="e0c4b-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="e0c4b-132">-JobId</span></span>
<span data-ttu-id="e0c4b-133">Alınacak işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c4b-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0c4b-134">-Profile</span></span>
<span data-ttu-id="e0c4b-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0c4b-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0c4b-137">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="e0c4b-137">-Subscription</span></span>
<span data-ttu-id="e0c4b-138">Alınacak HDInsight işlerini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c4b-139">CommonParameters</span></span>
<span data-ttu-id="e0c4b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0c4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c4b-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c4b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c4b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0c4b-142">INPUTS</span></span>

## <span data-ttu-id="e0c4b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0c4b-143">OUTPUTS</span></span>

## <span data-ttu-id="e0c4b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0c4b-144">NOTES</span></span>

## <span data-ttu-id="e0c4b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0c4b-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0c4b-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e0c4b-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="e0c4b-147">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e0c4b-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="e0c4b-148">Bekle-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e0c4b-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


