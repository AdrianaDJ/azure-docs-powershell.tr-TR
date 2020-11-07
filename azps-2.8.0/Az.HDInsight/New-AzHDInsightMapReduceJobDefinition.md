---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: c1dab20f44edfd4e3714e4465a0bf295e8e78fb5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751825"
---
# <span data-ttu-id="f0376-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f0376-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f0376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0376-102">SYNOPSIS</span></span>
<span data-ttu-id="f0376-103">MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0376-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="f0376-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0376-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0376-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0376-105">DESCRIPTION</span></span>
<span data-ttu-id="f0376-106">**New-AzHDInsightMapReduceJobDefinition** cmdlet 'ı, Azure HDInsight kümesiyle kullanılmak üzere yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f0376-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f0376-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0376-107">EXAMPLES</span></span>

### <span data-ttu-id="f0376-108">Örnek 1: MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f0376-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f0376-109">Bu komut bir MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0376-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="f0376-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0376-110">PARAMETERS</span></span>

### <span data-ttu-id="f0376-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="f0376-111">-Arguments</span></span>
<span data-ttu-id="f0376-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="f0376-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="f0376-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f0376-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="f0376-114">-ClassName</span></span>
<span data-ttu-id="f0376-115">JAR dosyasındaki iş sınıfını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="f0376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0376-116">-DefaultProfile</span></span>
<span data-ttu-id="f0376-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f0376-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0376-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="f0376-118">-Defines</span></span>
<span data-ttu-id="f0376-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="f0376-120">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="f0376-120">-Files</span></span>
<span data-ttu-id="f0376-121">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f0376-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="f0376-122">-JarFile</span></span>
<span data-ttu-id="f0376-123">İş için kullanılacak JAR dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="f0376-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="f0376-124">-JobName</span></span>
<span data-ttu-id="f0376-125">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="f0376-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="f0376-126">-LibJars</span></span>
<span data-ttu-id="f0376-127">İş için LIB JARS 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="f0376-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f0376-128">-StatusFolder</span></span>
<span data-ttu-id="f0376-129">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0376-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f0376-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0376-130">CommonParameters</span></span>
<span data-ttu-id="f0376-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0376-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0376-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0376-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0376-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0376-133">INPUTS</span></span>

### <span data-ttu-id="f0376-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f0376-134">None</span></span>

## <span data-ttu-id="f0376-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0376-135">OUTPUTS</span></span>

### <span data-ttu-id="f0376-136">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f0376-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f0376-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0376-137">NOTES</span></span>

## <span data-ttu-id="f0376-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0376-138">RELATED LINKS</span></span>

[<span data-ttu-id="f0376-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f0376-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


