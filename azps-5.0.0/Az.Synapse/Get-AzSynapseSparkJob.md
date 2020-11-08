---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277959"
---
# <span data-ttu-id="e2b89-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e2b89-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="e2b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b89-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b89-103">SYNAPSE Analizi Spark işini alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e2b89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2b89-104">SYNTAX</span></span>

### <span data-ttu-id="e2b89-105">Getparlak Jobsbyıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2b89-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b89-106">Getparlak Jobsbyıdfromparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="e2b89-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b89-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2b89-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b89-108">**Get-AzSynapseSparkJob** cmdlet 'ı bir Azure SYNAPSE Analytics Spark işini alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="e2b89-109">İş belirtmezseniz, bu cmdlet tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="e2b89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2b89-110">EXAMPLES</span></span>

### <span data-ttu-id="e2b89-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2b89-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="e2b89-112">Bu komut, Spark havuzunun altındaki tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="e2b89-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2b89-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="e2b89-114">Bu komut belirtilen KIMLIĞE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="e2b89-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e2b89-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="e2b89-116">Bu komut, belirtilen uygulama KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="e2b89-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e2b89-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="e2b89-118">Bu komut Spark havuzunun altındaki tüm işleri ardışık düzen ile alır.</span><span class="sxs-lookup"><span data-stu-id="e2b89-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="e2b89-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2b89-119">PARAMETERS</span></span>

### <span data-ttu-id="e2b89-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e2b89-120">-ApplicationId</span></span>
<span data-ttu-id="e2b89-121">Oturumun uygulama tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e2b89-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="e2b89-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b89-122">-DefaultProfile</span></span>
<span data-ttu-id="e2b89-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2b89-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b89-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="e2b89-124">-LivyId</span></span>
<span data-ttu-id="e2b89-125">Spark işinin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e2b89-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b89-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2b89-126">-Name</span></span>
<span data-ttu-id="e2b89-127">Spark işinin adı.</span><span class="sxs-lookup"><span data-stu-id="e2b89-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="e2b89-128">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="e2b89-128">-SparkPoolName</span></span>
<span data-ttu-id="e2b89-129">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e2b89-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b89-130">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="e2b89-130">-SparkPoolObject</span></span>
<span data-ttu-id="e2b89-131">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e2b89-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b89-132">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e2b89-132">-WorkspaceName</span></span>
<span data-ttu-id="e2b89-133">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e2b89-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b89-134">CommonParameters</span></span>
<span data-ttu-id="e2b89-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2b89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b89-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2b89-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b89-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2b89-137">INPUTS</span></span>

### <span data-ttu-id="e2b89-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e2b89-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e2b89-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2b89-139">OUTPUTS</span></span>

### <span data-ttu-id="e2b89-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e2b89-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="e2b89-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2b89-141">NOTES</span></span>

## <span data-ttu-id="e2b89-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2b89-142">RELATED LINKS</span></span>
