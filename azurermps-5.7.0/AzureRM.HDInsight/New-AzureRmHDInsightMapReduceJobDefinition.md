---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 3d40596b5797ca6b08b896e9ca973e491d130017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591003"
---
# <span data-ttu-id="df2af-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="df2af-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="df2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df2af-102">SYNOPSIS</span></span>
<span data-ttu-id="df2af-103">MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df2af-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df2af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df2af-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df2af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df2af-105">DESCRIPTION</span></span>
<span data-ttu-id="df2af-106">**New-AzureRmHDInsightMapReduceJobDefinition** cmdlet 'ı, Azure HDInsight kümesiyle kullanılmak üzere yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="df2af-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="df2af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df2af-107">EXAMPLES</span></span>

### <span data-ttu-id="df2af-108">Örnek 1: MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="df2af-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="df2af-109">Bu komut bir MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df2af-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="df2af-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df2af-110">PARAMETERS</span></span>

### <span data-ttu-id="df2af-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="df2af-111">-Arguments</span></span>
<span data-ttu-id="df2af-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="df2af-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="df2af-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="df2af-114">-ClassName</span></span>
<span data-ttu-id="df2af-115">JAR dosyasındaki iş sınıfını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-115">Specifies the job class in the JAR file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2af-116">-DefaultProfile</span></span>
<span data-ttu-id="df2af-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df2af-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df2af-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="df2af-118">-Defines</span></span>
<span data-ttu-id="df2af-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-120">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="df2af-120">-Files</span></span>
<span data-ttu-id="df2af-121">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="df2af-122">-JarFile</span></span>
<span data-ttu-id="df2af-123">İş için kullanılacak JAR dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-123">Specifies the JAR file to use for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="df2af-124">-JobName</span></span>
<span data-ttu-id="df2af-125">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="df2af-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="df2af-126">-LibJars</span></span>
<span data-ttu-id="df2af-127">İş için LIB JARS 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-127">Specifies the lib JARS for the job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2af-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="df2af-128">-StatusFolder</span></span>
<span data-ttu-id="df2af-129">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="df2af-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="df2af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2af-130">CommonParameters</span></span>
<span data-ttu-id="df2af-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df2af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2af-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2af-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2af-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df2af-133">INPUTS</span></span>

### <span data-ttu-id="df2af-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="df2af-134">None</span></span>
<span data-ttu-id="df2af-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="df2af-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df2af-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df2af-136">OUTPUTS</span></span>

### <span data-ttu-id="df2af-137">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="df2af-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="df2af-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df2af-138">NOTES</span></span>

## <span data-ttu-id="df2af-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df2af-139">RELATED LINKS</span></span>

[<span data-ttu-id="df2af-140">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df2af-140">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


