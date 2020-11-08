---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106434"
---
# <span data-ttu-id="4e637-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4e637-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="4e637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e637-102">SYNOPSIS</span></span>
<span data-ttu-id="4e637-103">Bir kümeye HTTP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4e637-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="4e637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e637-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e637-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e637-105">DESCRIPTION</span></span>
<span data-ttu-id="4e637-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="4e637-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4e637-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="4e637-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4e637-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e637-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4e637-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4e637-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4e637-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4e637-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4e637-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4e637-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4e637-112">**Revoke-AzureHDInsightHttpServicesAccess** CMDLET 'i ODBC, bir kümeleme, Oozie ve WebHCatalog Web SERVICES kümesine http erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4e637-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="4e637-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e637-113">EXAMPLES</span></span>

## <span data-ttu-id="4e637-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e637-114">PARAMETERS</span></span>

### <span data-ttu-id="4e637-115">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="4e637-115">-Certificate</span></span>
<span data-ttu-id="4e637-116">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="4e637-117">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="4e637-117">-Endpoint</span></span>
<span data-ttu-id="4e637-118">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4e637-119">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e637-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="4e637-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4e637-120">-HostedService</span></span>
<span data-ttu-id="4e637-121">Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="4e637-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4e637-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="4e637-123">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e637-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="4e637-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="4e637-124">-Location</span></span>
<span data-ttu-id="4e637-125">HDInsight kümesinin bulunduğu bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e637-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e637-126">-Name</span></span>
<span data-ttu-id="4e637-127">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="4e637-128">Bu cmdlet, bu parametrenin belirttiği kümeye HTTP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4e637-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e637-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="4e637-129">-Profile</span></span>
<span data-ttu-id="4e637-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e637-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4e637-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e637-132">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="4e637-132">-Subscription</span></span>
<span data-ttu-id="4e637-133">İptal edilecek HDInsight kümesini içeren abonelik hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e637-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="4e637-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e637-134">CommonParameters</span></span>
<span data-ttu-id="4e637-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e637-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e637-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e637-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e637-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e637-137">INPUTS</span></span>

## <span data-ttu-id="4e637-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e637-138">OUTPUTS</span></span>

## <span data-ttu-id="4e637-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e637-139">NOTES</span></span>

## <span data-ttu-id="4e637-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e637-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e637-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4e637-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


