---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 38eb1a7468b56507c5e5f2c0f68f04f1a1d2020d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764407"
---
# <span data-ttu-id="df858-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df858-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="df858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df858-102">SYNOPSIS</span></span>
<span data-ttu-id="df858-103">Belirtilen bir kümede tanımlı Azure HDInsight işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="df858-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df858-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df858-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df858-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df858-105">DESCRIPTION</span></span>
<span data-ttu-id="df858-106">**Start-AzureRMHDInsightJob** cmdlet 'i belirtilen bir kümede tanımlı bir Azure HDInsight işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="df858-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="df858-107">Bu bir MapReduce işi, bir akış MapReduce işi, bir kovan işi veya bir domuz işi olabilir.</span><span class="sxs-lookup"><span data-stu-id="df858-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="df858-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df858-108">EXAMPLES</span></span>

### <span data-ttu-id="df858-109">Örnek 1: belirtilen kümede iş başlatma</span><span class="sxs-lookup"><span data-stu-id="df858-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="df858-110">Bu komut,-Hadoop-001 adlı kümede bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="df858-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="df858-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df858-111">PARAMETERS</span></span>

### <span data-ttu-id="df858-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="df858-112">-ClusterName</span></span>
<span data-ttu-id="df858-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df858-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="df858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df858-114">-DefaultProfile</span></span>
<span data-ttu-id="df858-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df858-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df858-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="df858-116">-HttpCredential</span></span>
<span data-ttu-id="df858-117">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="df858-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="df858-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="df858-118">-JobDefinition</span></span>
<span data-ttu-id="df858-119">Azure HDInsight kümesinde başlayacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="df858-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="df858-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df858-120">-ResourceGroupName</span></span>
<span data-ttu-id="df858-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df858-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="df858-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df858-122">CommonParameters</span></span>
<span data-ttu-id="df858-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df858-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df858-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df858-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df858-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df858-125">INPUTS</span></span>

### <span data-ttu-id="df858-126">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="df858-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="df858-127">Parametreler: JobDefinition (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df858-127">Parameters: JobDefinition (ByValue)</span></span>

## <span data-ttu-id="df858-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df858-128">OUTPUTS</span></span>

### <span data-ttu-id="df858-129">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df858-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="df858-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df858-130">NOTES</span></span>

## <span data-ttu-id="df858-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df858-131">RELATED LINKS</span></span>

[<span data-ttu-id="df858-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df858-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="df858-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="df858-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="df858-134">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df858-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="df858-135">Bekle-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df858-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


