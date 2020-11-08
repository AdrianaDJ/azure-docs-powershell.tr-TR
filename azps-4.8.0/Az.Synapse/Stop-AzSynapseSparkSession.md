---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267953"
---
# <span data-ttu-id="fe273-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="fe273-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="fe273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe273-102">SYNOPSIS</span></span>
<span data-ttu-id="fe273-103">SYNAPSE Analytics Spark oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="fe273-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="fe273-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe273-104">SYNTAX</span></span>

### <span data-ttu-id="fe273-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe273-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe273-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe273-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe273-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe273-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe273-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe273-108">DESCRIPTION</span></span>
<span data-ttu-id="fe273-109">**Stop-AzSynapseSparkSession** cmdlet 'ı SYNAPSE Analytics Spark oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="fe273-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="fe273-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe273-110">EXAMPLES</span></span>

### <span data-ttu-id="fe273-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fe273-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="fe273-112">Bu komut, SYNAPSE Analytics Spark oturumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="fe273-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="fe273-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fe273-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="fe273-114">Bu komut SYNAPSE Analytics Spark oturumunu ardışık düzen aracılığıyla durdurur.</span><span class="sxs-lookup"><span data-stu-id="fe273-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="fe273-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fe273-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="fe273-116">Bu komut SYNAPSE Analytics Spark oturumunu ardışık düzen aracılığıyla durdurur.</span><span class="sxs-lookup"><span data-stu-id="fe273-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="fe273-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe273-117">PARAMETERS</span></span>

### <span data-ttu-id="fe273-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="fe273-118">-AsJob</span></span>
<span data-ttu-id="fe273-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fe273-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe273-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe273-120">-DefaultProfile</span></span>
<span data-ttu-id="fe273-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe273-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe273-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe273-122">-InputObject</span></span>
<span data-ttu-id="fe273-123">Spark oturum giriş nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="fe273-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe273-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="fe273-124">-LivyId</span></span>
<span data-ttu-id="fe273-125">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fe273-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe273-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fe273-126">-PassThru</span></span>
<span data-ttu-id="fe273-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="fe273-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fe273-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="fe273-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fe273-129">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="fe273-129">-SparkPoolName</span></span>
<span data-ttu-id="fe273-130">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="fe273-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe273-131">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="fe273-131">-SparkPoolObject</span></span>
<span data-ttu-id="fe273-132">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fe273-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe273-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="fe273-133">-WorkspaceName</span></span>
<span data-ttu-id="fe273-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="fe273-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe273-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe273-135">-Confirm</span></span>
<span data-ttu-id="fe273-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe273-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe273-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe273-137">-WhatIf</span></span>
<span data-ttu-id="fe273-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe273-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe273-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe273-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe273-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe273-140">CommonParameters</span></span>
<span data-ttu-id="fe273-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe273-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe273-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe273-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe273-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe273-143">INPUTS</span></span>

### <span data-ttu-id="fe273-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fe273-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="fe273-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="fe273-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="fe273-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe273-146">OUTPUTS</span></span>

### <span data-ttu-id="fe273-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe273-147">System.Boolean</span></span>

## <span data-ttu-id="fe273-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe273-148">NOTES</span></span>

## <span data-ttu-id="fe273-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe273-149">RELATED LINKS</span></span>
