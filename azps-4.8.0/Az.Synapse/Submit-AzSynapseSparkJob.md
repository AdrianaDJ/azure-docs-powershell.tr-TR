---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266197"
---
# <span data-ttu-id="4a6b1-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4a6b1-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4a6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6b1-103">SYNAPSE Analytics Spark işini gönderir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4a6b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a6b1-104">SYNTAX</span></span>

### <span data-ttu-id="4a6b1-105">Runparlak Jobparametersetname (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a6b1-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6b1-106">Runparlak Jobbyparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4a6b1-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a6b1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a6b1-107">DESCRIPTION</span></span>
<span data-ttu-id="4a6b1-108">**Submit-AzSynapseSparkJob** cmdlet 'ı bir Synapse Analytics Spark işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4a6b1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a6b1-109">EXAMPLES</span></span>

### <span data-ttu-id="4a6b1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a6b1-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4a6b1-111">Bu komut bir Synapse çözümleme Spark işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="4a6b1-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4a6b1-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4a6b1-113">Bu komut, SYNAPSE Analizi spark .NET işini gönderir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="4a6b1-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4a6b1-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4a6b1-115">Bu komut bir Synapse Analytics PySpark işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="4a6b1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a6b1-116">PARAMETERS</span></span>

### <span data-ttu-id="4a6b1-117">-Commanddoğrtası</span><span class="sxs-lookup"><span data-stu-id="4a6b1-117">-CommandLineArgument</span></span>
<span data-ttu-id="4a6b1-118">İş için isteğe bağlı bağımsız değişkenler.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-118">Optional arguments to the job.</span></span> <span data-ttu-id="4a6b1-119">Örneğin, "--Iteration 10000--Timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="4a6b1-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="4a6b1-120">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4a6b1-120">-Configuration</span></span>
<span data-ttu-id="4a6b1-121">Spark yapılandırma özellikleri.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="4a6b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6b1-122">-DefaultProfile</span></span>
<span data-ttu-id="4a6b1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6b1-124">-Yürüttorsayısı</span><span class="sxs-lookup"><span data-stu-id="4a6b1-124">-ExecutorCount</span></span>
<span data-ttu-id="4a6b1-125">İş için belirtilen Spark havuzunda ayrılacak yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-126">-Yürüttorsize</span><span class="sxs-lookup"><span data-stu-id="4a6b1-126">-ExecutorSize</span></span>
<span data-ttu-id="4a6b1-127">İş için belirtilen Spark havuzunda tahsis edilen yürüticileri için kullanılacak çekirdek ve bellek sayısı.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-128">-Dil</span><span class="sxs-lookup"><span data-stu-id="4a6b1-128">-Language</span></span>
<span data-ttu-id="4a6b1-129">Gönderecek işin dili.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="4a6b1-130">-MainClassName</span></span>
<span data-ttu-id="4a6b1-131">Tam nitelikli tanımlayıcı veya ana tanım dosyasındaki ana sınıf.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="4a6b1-132">Spark ve .NET Spark işi için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="4a6b1-133">Örneğin, "org. Apache. spark. örnekler. parlak Pi"</span><span class="sxs-lookup"><span data-stu-id="4a6b1-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4a6b1-134">-MainDefinitionFile</span></span>
<span data-ttu-id="4a6b1-135">İş için kullanılan ana dosya.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-135">The main file used for the job.</span></span>
<span data-ttu-id="4a6b1-136">Örneğin, " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="4a6b1-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="4a6b1-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a6b1-137">-Name</span></span>
<span data-ttu-id="4a6b1-138">Spark işinin adı.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="4a6b1-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="4a6b1-139">-ReferenceFile</span></span>
<span data-ttu-id="4a6b1-140">Ana tanım dosyasında başvuru için kullanılan ek dosyalar.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="4a6b1-141">Virgülle ayrılmış depolama URI listesi.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="4a6b1-142">Örneğin, " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="4a6b1-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="4a6b1-143">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="4a6b1-143">-SparkPoolName</span></span>
<span data-ttu-id="4a6b1-144">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-145">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="4a6b1-145">-SparkPoolObject</span></span>
<span data-ttu-id="4a6b1-146">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-147">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="4a6b1-147">-WorkspaceName</span></span>
<span data-ttu-id="4a6b1-148">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a6b1-149">-Confirm</span></span>
<span data-ttu-id="4a6b1-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6b1-151">-WhatIf</span></span>
<span data-ttu-id="4a6b1-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a6b1-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6b1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6b1-154">CommonParameters</span></span>
<span data-ttu-id="4a6b1-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6b1-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a6b1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6b1-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a6b1-157">INPUTS</span></span>

### <span data-ttu-id="4a6b1-158">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4a6b1-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="4a6b1-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a6b1-159">OUTPUTS</span></span>

### <span data-ttu-id="4a6b1-160">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4a6b1-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4a6b1-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a6b1-161">NOTES</span></span>

## <span data-ttu-id="4a6b1-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a6b1-162">RELATED LINKS</span></span>
