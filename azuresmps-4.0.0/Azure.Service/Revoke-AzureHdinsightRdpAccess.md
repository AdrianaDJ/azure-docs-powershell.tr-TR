---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105476"
---
# <span data-ttu-id="db29a-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="db29a-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="db29a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db29a-102">SYNOPSIS</span></span>
<span data-ttu-id="db29a-103">HDInsight kümesine RDP erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="db29a-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="db29a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db29a-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db29a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db29a-105">DESCRIPTION</span></span>
<span data-ttu-id="db29a-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="db29a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="db29a-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="db29a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="db29a-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="db29a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="db29a-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="db29a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="db29a-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="db29a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="db29a-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="db29a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="db29a-112">**Revoke-AzureHDInsightRdpAccess** cmdlet 'ı bir Azure HDInsight kümesine Uzak Masaüstü Protokolü (RDP) erişimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="db29a-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="db29a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db29a-113">EXAMPLES</span></span>

## <span data-ttu-id="db29a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db29a-114">PARAMETERS</span></span>

### <span data-ttu-id="db29a-115">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="db29a-115">-Certificate</span></span>
<span data-ttu-id="db29a-116">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="db29a-117">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="db29a-117">-Endpoint</span></span>
<span data-ttu-id="db29a-118">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="db29a-119">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="db29a-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="db29a-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="db29a-120">-HostedService</span></span>
<span data-ttu-id="db29a-121">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="db29a-122">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="db29a-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="db29a-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="db29a-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="db29a-124">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db29a-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="db29a-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="db29a-125">-Location</span></span>
<span data-ttu-id="db29a-126">Kümenin bulunduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="db29a-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="db29a-127">-Name</span></span>
<span data-ttu-id="db29a-128">Azure HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="db29a-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="db29a-129">-Profile</span></span>
<span data-ttu-id="db29a-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db29a-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="db29a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db29a-132">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="db29a-132">-Subscription</span></span>
<span data-ttu-id="db29a-133">Aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="db29a-133">Specifies a subscription.</span></span>
<span data-ttu-id="db29a-134">Bu cmdlet, bu parametrenin belirttiği aboneliğe Uzak Masaüstü Protokolü (RDP) erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="db29a-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="db29a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db29a-135">CommonParameters</span></span>
<span data-ttu-id="db29a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db29a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db29a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db29a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db29a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db29a-138">INPUTS</span></span>

## <span data-ttu-id="db29a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db29a-139">OUTPUTS</span></span>

## <span data-ttu-id="db29a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db29a-140">NOTES</span></span>

## <span data-ttu-id="db29a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db29a-141">RELATED LINKS</span></span>

[<span data-ttu-id="db29a-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="db29a-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


