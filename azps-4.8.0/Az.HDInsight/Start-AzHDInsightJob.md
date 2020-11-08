---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108086"
---
# <span data-ttu-id="f71f8-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f71f8-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="f71f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f71f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f71f8-103">Belirtilen bir kümede tanımlı Azure HDInsight işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f71f8-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="f71f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f71f8-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f71f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f71f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f71f8-106">**Start-AzHDInsightJob** cmdlet 'i belirtilen bir kümede tanımlı bir Azure HDInsight işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f71f8-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="f71f8-107">Bu bir MapReduce işi, bir akış MapReduce işi, bir kovan işi veya bir domuz işi olabilir.</span><span class="sxs-lookup"><span data-stu-id="f71f8-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="f71f8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f71f8-108">EXAMPLES</span></span>

### <span data-ttu-id="f71f8-109">Örnek 1: belirtilen kümede iş başlatma</span><span class="sxs-lookup"><span data-stu-id="f71f8-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f71f8-110">Bu komut,-Hadoop-001 adlı kümede bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="f71f8-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f71f8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f71f8-111">PARAMETERS</span></span>

### <span data-ttu-id="f71f8-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f71f8-112">-ClusterName</span></span>
<span data-ttu-id="f71f8-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f71f8-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f71f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71f8-114">-DefaultProfile</span></span>
<span data-ttu-id="f71f8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f71f8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f71f8-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f71f8-116">-HttpCredential</span></span>
<span data-ttu-id="f71f8-117">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f71f8-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f71f8-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="f71f8-118">-JobDefinition</span></span>
<span data-ttu-id="f71f8-119">Azure HDInsight kümesinde başlayacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f71f8-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f71f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f71f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="f71f8-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f71f8-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f71f8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71f8-122">CommonParameters</span></span>
<span data-ttu-id="f71f8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f71f8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71f8-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f71f8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71f8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f71f8-125">INPUTS</span></span>

### <span data-ttu-id="f71f8-126">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f71f8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="f71f8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f71f8-127">OUTPUTS</span></span>

### <span data-ttu-id="f71f8-128">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f71f8-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f71f8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f71f8-129">NOTES</span></span>

## <span data-ttu-id="f71f8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f71f8-130">RELATED LINKS</span></span>

[<span data-ttu-id="f71f8-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f71f8-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="f71f8-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f71f8-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f71f8-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f71f8-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="f71f8-134">Bekle-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f71f8-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


