---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: eebbe6fb233b0d6117411973e841cf39f2ae377d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592210"
---
# <span data-ttu-id="ed0f5-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="ed0f5-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="ed0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0f5-103">Belirli bir kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed0f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed0f5-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0f5-106">**Get-AzureRmHDInsightJobOutput** cmdlet 'ı, Azure HDInsight kümesiyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ed0f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed0f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0f5-108">Örnek 1: bir işin günlük çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="ed0f5-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="ed0f5-109">Bu komut,-Hadoop-001 adlı kümeden günlük çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ed0f5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed0f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ed0f5-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ed0f5-111">-ClusterName</span></span>
<span data-ttu-id="ed0f5-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ed0f5-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="ed0f5-113">-DefaultContainer</span></span>
<span data-ttu-id="ed0f5-114">Varsayılan kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="ed0f5-115">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed0f5-115">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ed0f5-116">Varsayılan depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-116">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="ed0f5-117">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed0f5-117">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ed0f5-118">Varsayılan depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-118">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="ed0f5-119">-Displami PutType</span><span class="sxs-lookup"><span data-stu-id="ed0f5-119">-DisplayOutputType</span></span>
<span data-ttu-id="ed0f5-120">İstenen iş çıktı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-120">Specifies the job output type being requested.</span></span>
<span data-ttu-id="ed0f5-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ed0f5-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed0f5-122">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="ed0f5-122">StandardOutput</span></span>
- <span data-ttu-id="ed0f5-123">Standar,</span><span class="sxs-lookup"><span data-stu-id="ed0f5-123">StandardError</span></span>

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

### <span data-ttu-id="ed0f5-124">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ed0f5-124">-HttpCredential</span></span>
<span data-ttu-id="ed0f5-125">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-125">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ed0f5-126">-JobId</span><span class="sxs-lookup"><span data-stu-id="ed0f5-126">-JobId</span></span>
<span data-ttu-id="ed0f5-127">Çıktısı getirilecek işin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-127">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="ed0f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed0f5-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ed0f5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0f5-130">-DefaultProfile</span></span>
<span data-ttu-id="ed0f5-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0f5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0f5-132">CommonParameters</span></span>
<span data-ttu-id="ed0f5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed0f5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0f5-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0f5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0f5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed0f5-135">INPUTS</span></span>

## <span data-ttu-id="ed0f5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed0f5-136">OUTPUTS</span></span>

### <span data-ttu-id="ed0f5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ed0f5-137">System.String</span></span>

## <span data-ttu-id="ed0f5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed0f5-138">NOTES</span></span>

## <span data-ttu-id="ed0f5-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed0f5-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed0f5-140">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ed0f5-140">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="ed0f5-141">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed0f5-141">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


