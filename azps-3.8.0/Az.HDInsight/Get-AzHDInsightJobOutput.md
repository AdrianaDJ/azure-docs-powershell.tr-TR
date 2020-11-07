---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938512"
---
# <span data-ttu-id="19024-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="19024-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="19024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19024-102">SYNOPSIS</span></span>
<span data-ttu-id="19024-103">Belirli bir kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="19024-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="19024-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19024-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19024-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19024-105">DESCRIPTION</span></span>
<span data-ttu-id="19024-106">**Get-AzHDInsightJobOutput** cmdlet 'ı, Azure HDInsight kümesiyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="19024-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="19024-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19024-107">EXAMPLES</span></span>

### <span data-ttu-id="19024-108">Örnek 1: bir işin günlük çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="19024-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="19024-109">Bu komut,-Hadoop-001 adlı kümeden günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="19024-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="19024-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19024-110">PARAMETERS</span></span>

### <span data-ttu-id="19024-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="19024-111">-ClusterName</span></span>
<span data-ttu-id="19024-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="19024-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="19024-113">-DefaultContainer</span></span>
<span data-ttu-id="19024-114">Varsayılan kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="19024-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19024-115">-DefaultProfile</span></span>
<span data-ttu-id="19024-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="19024-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19024-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="19024-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="19024-118">Varsayılan depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19024-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19024-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="19024-120">Varsayılan depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19024-121">-Displami PutType</span><span class="sxs-lookup"><span data-stu-id="19024-121">-DisplayOutputType</span></span>
<span data-ttu-id="19024-122">İstenen iş çıktı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="19024-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19024-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19024-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="19024-124">StandardOutput</span></span>
- <span data-ttu-id="19024-125">Standar,</span><span class="sxs-lookup"><span data-stu-id="19024-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19024-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="19024-126">-HttpCredential</span></span>
<span data-ttu-id="19024-127">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19024-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="19024-128">-JobId</span></span>
<span data-ttu-id="19024-129">Çıktısı getirilecek işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19024-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19024-130">-ResourceGroupName</span></span>
<span data-ttu-id="19024-131">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19024-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="19024-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19024-132">CommonParameters</span></span>
<span data-ttu-id="19024-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19024-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19024-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19024-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19024-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19024-135">INPUTS</span></span>

### <span data-ttu-id="19024-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="19024-136">None</span></span>

## <span data-ttu-id="19024-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19024-137">OUTPUTS</span></span>

### <span data-ttu-id="19024-138">System. String</span><span class="sxs-lookup"><span data-stu-id="19024-138">System.String</span></span>

## <span data-ttu-id="19024-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19024-139">NOTES</span></span>

## <span data-ttu-id="19024-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19024-140">RELATED LINKS</span></span>

[<span data-ttu-id="19024-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="19024-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="19024-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="19024-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


