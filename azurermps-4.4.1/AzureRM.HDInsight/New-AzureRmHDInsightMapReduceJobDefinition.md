---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594686"
---
# <span data-ttu-id="d8774-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d8774-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="d8774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8774-102">SYNOPSIS</span></span>
<span data-ttu-id="d8774-103">MapReduce iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8774-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8774-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8774-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8774-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8774-105">DESCRIPTION</span></span>
<span data-ttu-id="d8774-106">**New-AzureRmHDInsightMapReduceJobDefinition** cmdlet 'ı, Azure HDInsight kümesiyle kullanılmak üzere yeni bir Maduce işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d8774-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d8774-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8774-107">EXAMPLES</span></span>

### <span data-ttu-id="d8774-108">Örnek 1: MapReduce iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8774-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="d8774-109">Bu komut bir MapReduce iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8774-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="d8774-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8774-110">PARAMETERS</span></span>

### <span data-ttu-id="d8774-111">-Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d8774-111">-Arguments</span></span>
<span data-ttu-id="d8774-112">İş için bağımsız değişken dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d8774-113">Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.</span><span class="sxs-lookup"><span data-stu-id="d8774-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d8774-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="d8774-114">-ClassName</span></span>
<span data-ttu-id="d8774-115">JAR dosyasındaki iş sınıfını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="d8774-116">-Tanımlar</span><span class="sxs-lookup"><span data-stu-id="d8774-116">-Defines</span></span>
<span data-ttu-id="d8774-117">İş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="d8774-118">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="d8774-118">-Files</span></span>
<span data-ttu-id="d8774-119">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d8774-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="d8774-120">-JarFile</span></span>
<span data-ttu-id="d8774-121">İş için kullanılacak JAR dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="d8774-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="d8774-122">-JobName</span></span>
<span data-ttu-id="d8774-123">İşin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="d8774-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="d8774-124">-LibJars</span></span>
<span data-ttu-id="d8774-125">İş için LIB JARS 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="d8774-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d8774-126">-StatusFolder</span></span>
<span data-ttu-id="d8774-127">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8774-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d8774-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8774-128">-DefaultProfile</span></span>
<span data-ttu-id="d8774-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8774-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8774-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8774-130">CommonParameters</span></span>
<span data-ttu-id="d8774-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8774-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8774-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8774-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8774-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8774-133">INPUTS</span></span>

## <span data-ttu-id="d8774-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8774-134">OUTPUTS</span></span>

### <span data-ttu-id="d8774-135">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d8774-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="d8774-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8774-136">NOTES</span></span>

## <span data-ttu-id="d8774-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8774-137">RELATED LINKS</span></span>

[<span data-ttu-id="d8774-138">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d8774-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


