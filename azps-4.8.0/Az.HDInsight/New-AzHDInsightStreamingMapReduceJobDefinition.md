---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109059"
---
# <span data-ttu-id="ee9a9-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee9a9-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="ee9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9a9-103">Bir akış MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="ee9a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee9a9-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee9a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9a9-106">**New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir akış MapReduce iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ee9a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ee9a9-108">Örnek 1: bir akış MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ee9a9-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="ee9a9-109">Bu komut, bir akış MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="ee9a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ee9a9-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ee9a9-111">-Arguments</span></span>
<span data-ttu-id="ee9a9-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="ee9a9-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a9-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9a9-114">-CommandEnvironment</span></span>
<span data-ttu-id="ee9a9-115">İş çalışan düğümlerinde çalıştığında ayarlanacak komut satırı ortam değişkenleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9a9-116">-DefaultProfile</span></span>
<span data-ttu-id="ee9a9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee9a9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee9a9-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="ee9a9-118">-Defines</span></span>
<span data-ttu-id="ee9a9-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a9-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="ee9a9-120">-File</span></span>
<span data-ttu-id="ee9a9-121">Çalıştırılacak sorgu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="ee9a9-122">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="ee9a9-123">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="ee9a9-123">-Files</span></span>
<span data-ttu-id="ee9a9-124">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-124">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a9-125">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="ee9a9-125">-InputPath</span></span>
<span data-ttu-id="ee9a9-126">Giriş dosyalarının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a9-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="ee9a9-127">-Mapper</span></span>
<span data-ttu-id="ee9a9-128">Eşleyici dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="ee9a9-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ee9a9-129">-OutputPath</span></span>
<span data-ttu-id="ee9a9-130">İş çıkışının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="ee9a9-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="ee9a9-131">-Reducer</span></span>
<span data-ttu-id="ee9a9-132">Bir Reducer dosya adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="ee9a9-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ee9a9-133">-StatusFolder</span></span>
<span data-ttu-id="ee9a9-134">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="ee9a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9a9-135">CommonParameters</span></span>
<span data-ttu-id="ee9a9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee9a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9a9-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9a9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9a9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee9a9-138">INPUTS</span></span>

### <span data-ttu-id="ee9a9-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ee9a9-139">None</span></span>

## <span data-ttu-id="ee9a9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee9a9-140">OUTPUTS</span></span>

### <span data-ttu-id="ee9a9-141">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee9a9-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="ee9a9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee9a9-142">NOTES</span></span>

## <span data-ttu-id="ee9a9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee9a9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ee9a9-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ee9a9-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


