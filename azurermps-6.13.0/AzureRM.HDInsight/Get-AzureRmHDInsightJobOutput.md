---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590272"
---
# <span data-ttu-id="60ccb-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="60ccb-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="60ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="60ccb-103">Belirli bir kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="60ccb-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ccb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60ccb-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ccb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="60ccb-106">**Get-AzureRmHDInsightJobOutput** cmdlet 'ı, Azure HDInsight kümesiyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="60ccb-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="60ccb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="60ccb-108">Örnek 1: bir işin günlük çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="60ccb-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="60ccb-109">Bu komut,-Hadoop-001 adlı kümeden günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="60ccb-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="60ccb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="60ccb-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="60ccb-111">-ClusterName</span></span>
<span data-ttu-id="60ccb-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="60ccb-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="60ccb-113">-DefaultContainer</span></span>
<span data-ttu-id="60ccb-114">Varsayılan kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="60ccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ccb-115">-DefaultProfile</span></span>
<span data-ttu-id="60ccb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="60ccb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60ccb-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="60ccb-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="60ccb-118">Varsayılan depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="60ccb-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60ccb-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="60ccb-120">Varsayılan depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="60ccb-121">-Displami PutType</span><span class="sxs-lookup"><span data-stu-id="60ccb-121">-DisplayOutputType</span></span>
<span data-ttu-id="60ccb-122">İstenen iş çıktı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="60ccb-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="60ccb-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60ccb-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="60ccb-124">StandardOutput</span></span>
- <span data-ttu-id="60ccb-125">Standar,</span><span class="sxs-lookup"><span data-stu-id="60ccb-125">StandardError</span></span>

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

### <span data-ttu-id="60ccb-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="60ccb-126">-HttpCredential</span></span>
<span data-ttu-id="60ccb-127">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="60ccb-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="60ccb-128">-JobId</span></span>
<span data-ttu-id="60ccb-129">Çıktısı getirilecek işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="60ccb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ccb-130">-ResourceGroupName</span></span>
<span data-ttu-id="60ccb-131">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60ccb-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="60ccb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ccb-132">CommonParameters</span></span>
<span data-ttu-id="60ccb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60ccb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ccb-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ccb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ccb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60ccb-135">INPUTS</span></span>

### <span data-ttu-id="60ccb-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="60ccb-136">None</span></span>

## <span data-ttu-id="60ccb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60ccb-137">OUTPUTS</span></span>

### <span data-ttu-id="60ccb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60ccb-138">System.String</span></span>

## <span data-ttu-id="60ccb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60ccb-139">NOTES</span></span>

## <span data-ttu-id="60ccb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60ccb-140">RELATED LINKS</span></span>

[<span data-ttu-id="60ccb-141">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="60ccb-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="60ccb-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="60ccb-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


