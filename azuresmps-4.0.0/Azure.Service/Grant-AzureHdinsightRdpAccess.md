---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106262"
---
# <span data-ttu-id="ab298-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ab298-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="ab298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab298-102">SYNOPSIS</span></span>
<span data-ttu-id="ab298-103">HDInsight kümesine RDP erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="ab298-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="ab298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab298-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab298-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab298-105">DESCRIPTION</span></span>
<span data-ttu-id="ab298-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="ab298-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ab298-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ab298-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ab298-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab298-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ab298-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ab298-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ab298-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ab298-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ab298-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab298-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ab298-112">**Grant-AzureHDInsightRdpAccess** cmdlet 'i, bir Azure HDInsight kümesine Uzak Masaüstü Protokolü (RDP) erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="ab298-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ab298-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab298-113">EXAMPLES</span></span>

## <span data-ttu-id="ab298-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab298-114">PARAMETERS</span></span>

### <span data-ttu-id="ab298-115">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="ab298-115">-Certificate</span></span>
<span data-ttu-id="ab298-116">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ab298-117">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="ab298-117">-Endpoint</span></span>
<span data-ttu-id="ab298-118">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ab298-119">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="ab298-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ab298-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ab298-120">-HostedService</span></span>
<span data-ttu-id="ab298-121">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ab298-122">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="ab298-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="ab298-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ab298-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="ab298-124">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab298-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ab298-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="ab298-125">-Location</span></span>
<span data-ttu-id="ab298-126">Kümenin bulunduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="ab298-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab298-127">-Name</span></span>
<span data-ttu-id="ab298-128">Azure HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="ab298-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab298-129">-Profile</span></span>
<span data-ttu-id="ab298-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ab298-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ab298-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab298-132">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="ab298-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="ab298-133">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için **Tarih saat** sonu</span><span class="sxs-lookup"><span data-stu-id="ab298-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab298-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ab298-134">-RdpCredential</span></span>
<span data-ttu-id="ab298-135">Bir kümeye RDP erişimi için kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-135">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="ab298-136">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="ab298-136">-Subscription</span></span>
<span data-ttu-id="ab298-137">Erişim verilecek HDInsight kümesini içeren aboneliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab298-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="ab298-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab298-138">CommonParameters</span></span>
<span data-ttu-id="ab298-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab298-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab298-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab298-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab298-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab298-141">INPUTS</span></span>

## <span data-ttu-id="ab298-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab298-142">OUTPUTS</span></span>

## <span data-ttu-id="ab298-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab298-143">NOTES</span></span>

## <span data-ttu-id="ab298-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab298-144">RELATED LINKS</span></span>

[<span data-ttu-id="ab298-145">Revoke-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ab298-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


