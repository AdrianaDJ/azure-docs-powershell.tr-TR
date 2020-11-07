---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 2fa3ae6cd48887f377ea4bdb6ce36001afe29b5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762526"
---
# <span data-ttu-id="d9068-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9068-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="d9068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9068-102">SYNOPSIS</span></span>
<span data-ttu-id="d9068-103">Bir kümeden işlerin listesini alır ve bunları ters sırada listeler veya belirli bir iş alır.</span><span class="sxs-lookup"><span data-stu-id="d9068-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9068-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9068-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9068-105">DESCRIPTION</span></span>
<span data-ttu-id="d9068-106">**Get-AzureRmHDInsightJob** cmdlet 'i, belirli bir Azure HDInsight kümesinin en son işlerini, listenin en son işine sahip olacak şekilde ters sırada alır.</span><span class="sxs-lookup"><span data-stu-id="d9068-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="d9068-107">*JobId* parametresini sağlayarak belirli bir iş edinin.</span><span class="sxs-lookup"><span data-stu-id="d9068-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="d9068-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9068-108">EXAMPLES</span></span>

### <span data-ttu-id="d9068-109">Örnek 1: belirtilen Azure HDInsight kümesinin en son işlerini alma</span><span class="sxs-lookup"><span data-stu-id="d9068-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d9068-110">Bu komut,-Hadoop-001 adlı kümenin tüm son işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d9068-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d9068-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9068-111">PARAMETERS</span></span>

### <span data-ttu-id="d9068-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9068-112">-ClusterName</span></span>
<span data-ttu-id="d9068-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9068-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9068-114">-DefaultProfile</span></span>
<span data-ttu-id="d9068-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9068-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d9068-116">-HttpCredential</span></span>
<span data-ttu-id="d9068-117">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9068-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9068-118">-JobId</span></span>
<span data-ttu-id="d9068-119">Alınacak işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9068-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="d9068-120">-NumOfJobs</span></span>
<span data-ttu-id="d9068-121">Alınacak iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9068-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9068-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9068-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9068-123">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9068-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9068-124">CommonParameters</span></span>
<span data-ttu-id="d9068-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9068-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9068-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9068-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9068-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9068-127">INPUTS</span></span>

### <span data-ttu-id="d9068-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d9068-128">None</span></span>
<span data-ttu-id="d9068-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d9068-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9068-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9068-130">OUTPUTS</span></span>

### <span data-ttu-id="d9068-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9068-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d9068-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9068-132">NOTES</span></span>

## <span data-ttu-id="d9068-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9068-133">RELATED LINKS</span></span>

[<span data-ttu-id="d9068-134">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d9068-134">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d9068-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9068-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="d9068-136">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9068-136">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="d9068-137">Bekle-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9068-137">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


