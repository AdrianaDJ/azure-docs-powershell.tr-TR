---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267954"
---
# <span data-ttu-id="adbb7-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="adbb7-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="adbb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="adbb7-103">SYNAPSE Analytics Spark işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="adbb7-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="adbb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adbb7-104">SYNTAX</span></span>

### <span data-ttu-id="adbb7-105">Stopparlak Jobbyıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="adbb7-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbb7-106">Stopmini iş Byıdfromparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="adbb7-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbb7-107">Stopminijobbyıdfrominputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="adbb7-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbb7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="adbb7-108">DESCRIPTION</span></span>
<span data-ttu-id="adbb7-109">**Stop-AzSynapseSparkJob** cmdlet 'ı bir Synapse Analytics Spark işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="adbb7-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="adbb7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adbb7-110">EXAMPLES</span></span>

### <span data-ttu-id="adbb7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="adbb7-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="adbb7-112">Bu komut SYNAPSE Analytics Spark işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="adbb7-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="adbb7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="adbb7-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="adbb7-114">Bu komut SYNAPSE Analytics Spark işini ardışık düzen aracılığıyla iptal eder.</span><span class="sxs-lookup"><span data-stu-id="adbb7-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="adbb7-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="adbb7-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="adbb7-116">Bu komut SYNAPSE Analytics Spark işini ardışık düzen aracılığıyla iptal eder.</span><span class="sxs-lookup"><span data-stu-id="adbb7-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="adbb7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adbb7-117">PARAMETERS</span></span>

### <span data-ttu-id="adbb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbb7-118">-DefaultProfile</span></span>
<span data-ttu-id="adbb7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="adbb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbb7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="adbb7-120">-Force</span></span>
<span data-ttu-id="adbb7-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="adbb7-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="adbb7-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="adbb7-122">-LivyId</span></span>
<span data-ttu-id="adbb7-123">Spark işinin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="adbb7-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbb7-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="adbb7-124">-PassThru</span></span>
<span data-ttu-id="adbb7-125">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="adbb7-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="adbb7-126">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="adbb7-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="adbb7-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="adbb7-127">-SparkJobObject</span></span>
<span data-ttu-id="adbb7-128">Spark iş girişi nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="adbb7-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adbb7-129">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="adbb7-129">-SparkPoolName</span></span>
<span data-ttu-id="adbb7-130">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="adbb7-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbb7-131">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="adbb7-131">-SparkPoolObject</span></span>
<span data-ttu-id="adbb7-132">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="adbb7-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adbb7-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="adbb7-133">-WorkspaceName</span></span>
<span data-ttu-id="adbb7-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="adbb7-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adbb7-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="adbb7-135">-Confirm</span></span>
<span data-ttu-id="adbb7-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="adbb7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbb7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbb7-137">-WhatIf</span></span>
<span data-ttu-id="adbb7-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="adbb7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbb7-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="adbb7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbb7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbb7-140">CommonParameters</span></span>
<span data-ttu-id="adbb7-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adbb7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbb7-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="adbb7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbb7-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adbb7-143">INPUTS</span></span>

### <span data-ttu-id="adbb7-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="adbb7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="adbb7-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="adbb7-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="adbb7-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adbb7-146">OUTPUTS</span></span>

### <span data-ttu-id="adbb7-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adbb7-147">System.Boolean</span></span>

## <span data-ttu-id="adbb7-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adbb7-148">NOTES</span></span>

## <span data-ttu-id="adbb7-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adbb7-149">RELATED LINKS</span></span>
