---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109062"
---
# <span data-ttu-id="64663-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="64663-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="64663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64663-102">SYNOPSIS</span></span>
<span data-ttu-id="64663-103">MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64663-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="64663-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64663-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64663-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64663-105">DESCRIPTION</span></span>
<span data-ttu-id="64663-106">**New-AzHDInsightMapReduceJobDefinition** cmdlet 'ı, Azure HDInsight kümesiyle kullanılmak üzere yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="64663-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="64663-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64663-107">EXAMPLES</span></span>

### <span data-ttu-id="64663-108">Örnek 1: MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="64663-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="64663-109">Bu komut bir MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64663-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="64663-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64663-110">PARAMETERS</span></span>

### <span data-ttu-id="64663-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="64663-111">-Arguments</span></span>
<span data-ttu-id="64663-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="64663-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="64663-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="64663-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="64663-114">-ClassName</span></span>
<span data-ttu-id="64663-115">JAR dosyasındaki iş sınıfını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="64663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64663-116">-DefaultProfile</span></span>
<span data-ttu-id="64663-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="64663-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64663-118">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="64663-118">-Defines</span></span>
<span data-ttu-id="64663-119">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="64663-120">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="64663-120">-Files</span></span>
<span data-ttu-id="64663-121">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="64663-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="64663-122">-JarFile</span></span>
<span data-ttu-id="64663-123">İş için kullanılacak JAR dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="64663-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="64663-124">-JobName</span></span>
<span data-ttu-id="64663-125">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="64663-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="64663-126">-LibJars</span></span>
<span data-ttu-id="64663-127">İş için LIB JARS 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="64663-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="64663-128">-StatusFolder</span></span>
<span data-ttu-id="64663-129">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="64663-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="64663-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64663-130">CommonParameters</span></span>
<span data-ttu-id="64663-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64663-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64663-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64663-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64663-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64663-133">INPUTS</span></span>

### <span data-ttu-id="64663-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="64663-134">None</span></span>

## <span data-ttu-id="64663-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64663-135">OUTPUTS</span></span>

### <span data-ttu-id="64663-136">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="64663-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="64663-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64663-137">NOTES</span></span>

## <span data-ttu-id="64663-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64663-138">RELATED LINKS</span></span>

[<span data-ttu-id="64663-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64663-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


