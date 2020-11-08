---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106351"
---
# <span data-ttu-id="72805-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="72805-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="72805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72805-102">SYNOPSIS</span></span>
<span data-ttu-id="72805-103">HDInsight hizmetine özgü özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="72805-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="72805-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72805-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="72805-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72805-105">DESCRIPTION</span></span>
<span data-ttu-id="72805-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="72805-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="72805-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="72805-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="72805-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="72805-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="72805-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="72805-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="72805-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="72805-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="72805-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="72805-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="72805-112">**Get-AzureHDInsightProperties** cmdlet 'i, kullanılabilir Azure bölgelerinin, HDInsight küme sürümlerinin ve kullanılabilir işlem kapasitelerinin listesi gibi bir Azure HDInsight hizmetine özgü özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="72805-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="72805-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72805-113">EXAMPLES</span></span>

### <span data-ttu-id="72805-114">Örnek 1: bir aboneliğin HDInsight özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="72805-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="72805-115">İlk komut geçerli Azure aboneliğinin adını alır ve $SubName değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="72805-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="72805-116">İkinci komut $SubName aboneliğinin HDInsight özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="72805-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="72805-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72805-117">PARAMETERS</span></span>

### <span data-ttu-id="72805-118">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="72805-118">-Certificate</span></span>
<span data-ttu-id="72805-119">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72805-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="72805-120">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="72805-120">-Endpoint</span></span>
<span data-ttu-id="72805-121">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="72805-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="72805-122">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="72805-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="72805-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="72805-123">-HostedService</span></span>
<span data-ttu-id="72805-124">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72805-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="72805-125">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="72805-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="72805-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="72805-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="72805-127">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72805-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="72805-128">-Konumlar</span><span class="sxs-lookup"><span data-stu-id="72805-128">-Locations</span></span>
<span data-ttu-id="72805-129">Bu cmdlet 'in, HDInsight hizmetinin kullanılabilir olduğu Azure bölgelerinin listesini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72805-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72805-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="72805-130">-Profile</span></span>
<span data-ttu-id="72805-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72805-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72805-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="72805-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72805-133">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="72805-133">-Subscription</span></span>
<span data-ttu-id="72805-134">Alınacak HDInsight özelliklerini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="72805-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="72805-135">-Sürümler</span><span class="sxs-lookup"><span data-stu-id="72805-135">-Versions</span></span>
<span data-ttu-id="72805-136">Bu cmdlet 'in, bir abonelik için hizmette bulunan HDInsight küme sürümlerinin listesini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72805-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72805-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72805-137">CommonParameters</span></span>
<span data-ttu-id="72805-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72805-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72805-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72805-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72805-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72805-140">INPUTS</span></span>

## <span data-ttu-id="72805-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72805-141">OUTPUTS</span></span>

## <span data-ttu-id="72805-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72805-142">NOTES</span></span>

## <span data-ttu-id="72805-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72805-143">RELATED LINKS</span></span>

