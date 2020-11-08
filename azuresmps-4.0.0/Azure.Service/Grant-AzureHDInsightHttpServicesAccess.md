---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106498"
---
# <span data-ttu-id="0cd0e-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0cd0e-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="0cd0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cd0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd0e-103">Bir kümeye HTTP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="0cd0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cd0e-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0cd0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cd0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd0e-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="0cd0e-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="0cd0e-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="0cd0e-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="0cd0e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="0cd0e-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="0cd0e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="0cd0e-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0cd0e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="0cd0e-112">**Grant-AzureHDInsightHttpServicesAccess** cmdlet 'ı, ODBC, ambarı, Oozie ve Web Hizmetleri 'ni kullanarak bir Azure HDıNSIGHT kümesine http erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="0cd0e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cd0e-113">EXAMPLES</span></span>

## <span data-ttu-id="0cd0e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cd0e-114">PARAMETERS</span></span>

### <span data-ttu-id="0cd0e-115">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="0cd0e-115">-Certificate</span></span>
<span data-ttu-id="0cd0e-116">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="0cd0e-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="0cd0e-117">-Credential</span></span>
<span data-ttu-id="0cd0e-118">HTTP erişimi için bir Kullanıcı adı ve parola belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd0e-119">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="0cd0e-119">-Endpoint</span></span>
<span data-ttu-id="0cd0e-120">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="0cd0e-121">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="0cd0e-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="0cd0e-122">-HostedService</span></span>
<span data-ttu-id="0cd0e-123">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="0cd0e-124">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="0cd0e-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="0cd0e-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="0cd0e-126">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="0cd0e-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="0cd0e-127">-Location</span></span>
<span data-ttu-id="0cd0e-128">Kümenin bulunduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="0cd0e-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cd0e-129">-Name</span></span>
<span data-ttu-id="0cd0e-130">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="0cd0e-131">Bu cmdlet, bu parametrenin belirttiği kümeye HTTP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="0cd0e-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="0cd0e-132">-Profile</span></span>
<span data-ttu-id="0cd0e-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0cd0e-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0cd0e-135">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="0cd0e-135">-Subscription</span></span>
<span data-ttu-id="0cd0e-136">Erişim verilecek HDInsight kümesini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="0cd0e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd0e-137">CommonParameters</span></span>
<span data-ttu-id="0cd0e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cd0e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd0e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd0e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd0e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cd0e-140">INPUTS</span></span>

## <span data-ttu-id="0cd0e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cd0e-141">OUTPUTS</span></span>

## <span data-ttu-id="0cd0e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cd0e-142">NOTES</span></span>

## <span data-ttu-id="0cd0e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cd0e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0cd0e-144">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0cd0e-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


