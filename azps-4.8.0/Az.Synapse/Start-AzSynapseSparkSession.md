---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267960"
---
# <span data-ttu-id="6f89a-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6f89a-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="6f89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f89a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f89a-103">SYNAPSE Analytics Spark oturumunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="6f89a-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6f89a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f89a-104">SYNTAX</span></span>

### <span data-ttu-id="6f89a-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f89a-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f89a-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f89a-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f89a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f89a-107">DESCRIPTION</span></span>
<span data-ttu-id="6f89a-108">**Start-AzSynapseSparkSession** cmdlet 'ı SYNAPSE Analytics Spark oturumunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="6f89a-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6f89a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f89a-109">EXAMPLES</span></span>

### <span data-ttu-id="6f89a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f89a-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="6f89a-111">Bu komut, bir Azure SYNAPSE Analytics Spark oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="6f89a-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="6f89a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6f89a-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="6f89a-113">Bu komut, ardışık düzen aracılığıyla Azure SYNAPSE Analytics Spark oturumunu başlatır.</span><span class="sxs-lookup"><span data-stu-id="6f89a-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="6f89a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f89a-114">PARAMETERS</span></span>

### <span data-ttu-id="6f89a-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6f89a-115">-AsJob</span></span>
<span data-ttu-id="6f89a-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6f89a-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-117">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6f89a-117">-Configuration</span></span>
<span data-ttu-id="6f89a-118">Spark yapılandırma özellikleri.</span><span class="sxs-lookup"><span data-stu-id="6f89a-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="6f89a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f89a-119">-DefaultProfile</span></span>
<span data-ttu-id="6f89a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f89a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f89a-121">-Yürüttorsayısı</span><span class="sxs-lookup"><span data-stu-id="6f89a-121">-ExecutorCount</span></span>
<span data-ttu-id="6f89a-122">İş için belirtilen Spark havuzunda ayrılacak yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="6f89a-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="6f89a-123">-Yürüttorsize</span><span class="sxs-lookup"><span data-stu-id="6f89a-123">-ExecutorSize</span></span>
<span data-ttu-id="6f89a-124">İş için belirtilen Spark havuzunda tahsis edilen yürüticileri için kullanılacak çekirdek ve bellek sayısı.</span><span class="sxs-lookup"><span data-stu-id="6f89a-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="6f89a-125">-Dil</span><span class="sxs-lookup"><span data-stu-id="6f89a-125">-Language</span></span>
<span data-ttu-id="6f89a-126">Yürütme kodunun dili.</span><span class="sxs-lookup"><span data-stu-id="6f89a-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f89a-127">-Name</span></span>
<span data-ttu-id="6f89a-128">Spark oturumunun adı.</span><span class="sxs-lookup"><span data-stu-id="6f89a-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="6f89a-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="6f89a-129">-ReferenceFile</span></span>
<span data-ttu-id="6f89a-130">Ana tanım dosyasında başvuru için kullanılan ek dosyalar.</span><span class="sxs-lookup"><span data-stu-id="6f89a-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="6f89a-131">Virgülle ayrılmış depolama URI listesi.</span><span class="sxs-lookup"><span data-stu-id="6f89a-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="6f89a-132">Örneğin, " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="6f89a-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="6f89a-133">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="6f89a-133">-SparkPoolName</span></span>
<span data-ttu-id="6f89a-134">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6f89a-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-135">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="6f89a-135">-SparkPoolObject</span></span>
<span data-ttu-id="6f89a-136">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6f89a-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-137">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6f89a-137">-WorkspaceName</span></span>
<span data-ttu-id="6f89a-138">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="6f89a-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f89a-139">-Confirm</span></span>
<span data-ttu-id="6f89a-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f89a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f89a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f89a-141">-WhatIf</span></span>
<span data-ttu-id="6f89a-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f89a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f89a-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f89a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f89a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f89a-144">CommonParameters</span></span>
<span data-ttu-id="6f89a-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f89a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f89a-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f89a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f89a-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f89a-147">INPUTS</span></span>

### <span data-ttu-id="6f89a-148">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6f89a-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6f89a-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f89a-149">OUTPUTS</span></span>

### <span data-ttu-id="6f89a-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6f89a-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="6f89a-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f89a-151">NOTES</span></span>

## <span data-ttu-id="6f89a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f89a-152">RELATED LINKS</span></span>
