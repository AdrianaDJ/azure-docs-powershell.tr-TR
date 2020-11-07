---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 22ddeeffd696de260e13c1c817afedfabe1887a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763858"
---
# <span data-ttu-id="15511-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="15511-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="15511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15511-102">SYNOPSIS</span></span>
<span data-ttu-id="15511-103">Bir akış MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15511-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15511-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15511-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15511-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15511-105">DESCRIPTION</span></span>
<span data-ttu-id="15511-106">**New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir akış MapReduce iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="15511-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="15511-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15511-107">EXAMPLES</span></span>

### <span data-ttu-id="15511-108">Örnek 1: bir akış MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15511-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="15511-109">Bu komut, bir akış MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15511-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="15511-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15511-110">PARAMETERS</span></span>

### <span data-ttu-id="15511-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="15511-111">-Arguments</span></span>
<span data-ttu-id="15511-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="15511-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="15511-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="15511-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="15511-114">-CommandEnvironment</span></span>
<span data-ttu-id="15511-115">İş çalışan düğümlerinde çalıştığında ayarlanacak komut satırı ortam değişkenleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="15511-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15511-116">-DefaultProfile</span></span>
<span data-ttu-id="15511-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="15511-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15511-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="15511-118">-Defines</span></span>
<span data-ttu-id="15511-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="15511-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="15511-120">-File</span></span>
<span data-ttu-id="15511-121">Çalıştırılacak sorgu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="15511-122">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15511-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="15511-123">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="15511-123">-Files</span></span>
<span data-ttu-id="15511-124">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="15511-125">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="15511-125">-InputPath</span></span>
<span data-ttu-id="15511-126">Giriş dosyalarının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="15511-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="15511-127">-Mapper</span></span>
<span data-ttu-id="15511-128">Eşleyici dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="15511-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="15511-129">-OutputPath</span></span>
<span data-ttu-id="15511-130">İş çıkışının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="15511-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="15511-131">-Reducer</span></span>
<span data-ttu-id="15511-132">Bir Reducer dosya adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="15511-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="15511-133">-StatusFolder</span></span>
<span data-ttu-id="15511-134">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15511-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="15511-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15511-135">CommonParameters</span></span>
<span data-ttu-id="15511-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15511-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15511-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15511-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15511-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15511-138">INPUTS</span></span>

### <span data-ttu-id="15511-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15511-139">None</span></span>

## <span data-ttu-id="15511-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15511-140">OUTPUTS</span></span>

### <span data-ttu-id="15511-141">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="15511-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="15511-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15511-142">NOTES</span></span>

## <span data-ttu-id="15511-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15511-143">RELATED LINKS</span></span>

[<span data-ttu-id="15511-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="15511-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


