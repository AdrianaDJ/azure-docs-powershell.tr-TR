---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 06d0a7070b90adde5fdf0f65b90e083d25aaba59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916636"
---
# <span data-ttu-id="304a5-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="304a5-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="304a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="304a5-102">SYNOPSIS</span></span>
<span data-ttu-id="304a5-103">Bir kümeden işlerin listesini alır ve bunları ters sırada listeler veya belirli bir iş alır.</span><span class="sxs-lookup"><span data-stu-id="304a5-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="304a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="304a5-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="304a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="304a5-105">DESCRIPTION</span></span>
<span data-ttu-id="304a5-106">**Get-AzHDInsightJob** cmdlet 'i, belirli bir Azure HDInsight kümesinin en son işlerini, listenin en son işine sahip olacak şekilde ters sırada alır.</span><span class="sxs-lookup"><span data-stu-id="304a5-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="304a5-107">*JobId* parametresini sağlayarak belirli bir iş edinin.</span><span class="sxs-lookup"><span data-stu-id="304a5-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="304a5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="304a5-108">EXAMPLES</span></span>

### <span data-ttu-id="304a5-109">Örnek 1: belirtilen Azure HDInsight kümesinin en son işlerini alma</span><span class="sxs-lookup"><span data-stu-id="304a5-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="304a5-110">Bu komut,-Hadoop-001 adlı kümenin tüm son işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="304a5-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="304a5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="304a5-111">PARAMETERS</span></span>

### <span data-ttu-id="304a5-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="304a5-112">-ClusterName</span></span>
<span data-ttu-id="304a5-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="304a5-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304a5-114">-DefaultProfile</span></span>
<span data-ttu-id="304a5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="304a5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="304a5-116">-HttpCredential</span></span>
<span data-ttu-id="304a5-117">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="304a5-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="304a5-118">-JobId</span></span>
<span data-ttu-id="304a5-119">Alınacak işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="304a5-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="304a5-120">-NumOfJobs</span></span>
<span data-ttu-id="304a5-121">Alınacak iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="304a5-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="304a5-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="304a5-123">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304a5-124">CommonParameters</span></span>
<span data-ttu-id="304a5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="304a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304a5-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="304a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304a5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="304a5-127">INPUTS</span></span>

### <span data-ttu-id="304a5-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="304a5-128">None</span></span>

## <span data-ttu-id="304a5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="304a5-129">OUTPUTS</span></span>

### <span data-ttu-id="304a5-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="304a5-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="304a5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="304a5-131">NOTES</span></span>

## <span data-ttu-id="304a5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="304a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="304a5-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="304a5-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="304a5-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="304a5-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="304a5-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="304a5-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="304a5-136">Bekle-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="304a5-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


