---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277835"
---
# <span data-ttu-id="01127-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="01127-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="01127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01127-102">SYNOPSIS</span></span>
<span data-ttu-id="01127-103">Bir akış MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01127-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="01127-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01127-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01127-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01127-105">DESCRIPTION</span></span>
<span data-ttu-id="01127-106">**New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir akış MapReduce iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="01127-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="01127-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01127-107">EXAMPLES</span></span>

### <span data-ttu-id="01127-108">Örnek 1: bir akış MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="01127-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="01127-109">Bu komut, bir akış MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01127-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="01127-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01127-110">PARAMETERS</span></span>

### <span data-ttu-id="01127-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="01127-111">-Arguments</span></span>
<span data-ttu-id="01127-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="01127-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="01127-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="01127-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="01127-114">-CommandEnvironment</span></span>
<span data-ttu-id="01127-115">İş çalışan düğümlerinde çalıştığında ayarlanacak komut satırı ortam değişkenleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="01127-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01127-116">-DefaultProfile</span></span>
<span data-ttu-id="01127-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01127-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01127-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="01127-118">-Defines</span></span>
<span data-ttu-id="01127-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="01127-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="01127-120">-File</span></span>
<span data-ttu-id="01127-121">Çalıştırılacak sorgu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="01127-122">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01127-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="01127-123">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="01127-123">-Files</span></span>
<span data-ttu-id="01127-124">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="01127-125">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="01127-125">-InputPath</span></span>
<span data-ttu-id="01127-126">Giriş dosyalarının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="01127-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="01127-127">-Mapper</span></span>
<span data-ttu-id="01127-128">Eşleyici dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="01127-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="01127-129">-OutputPath</span></span>
<span data-ttu-id="01127-130">İş çıkışının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="01127-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="01127-131">-Reducer</span></span>
<span data-ttu-id="01127-132">Bir Reducer dosya adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="01127-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="01127-133">-StatusFolder</span></span>
<span data-ttu-id="01127-134">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01127-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="01127-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01127-135">CommonParameters</span></span>
<span data-ttu-id="01127-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01127-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01127-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01127-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01127-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01127-138">INPUTS</span></span>

### <span data-ttu-id="01127-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="01127-139">None</span></span>

## <span data-ttu-id="01127-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01127-140">OUTPUTS</span></span>

### <span data-ttu-id="01127-141">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="01127-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="01127-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01127-142">NOTES</span></span>

## <span data-ttu-id="01127-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01127-143">RELATED LINKS</span></span>

[<span data-ttu-id="01127-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="01127-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


