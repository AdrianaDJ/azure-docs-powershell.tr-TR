---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268940"
---
# <span data-ttu-id="66fe8-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="66fe8-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="66fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="66fe8-103">SYNAPSE Analytics Spark oturumunun zaman aşımını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="66fe8-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="66fe8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66fe8-104">SYNTAX</span></span>

### <span data-ttu-id="66fe8-105">ResetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66fe8-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fe8-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fe8-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fe8-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66fe8-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fe8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="66fe8-109">**Remove-AzSynapseSparkSessionTimeout** cmdlet 'ı SYNAPSE Analytics Spark oturumunun zaman aşımını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="66fe8-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="66fe8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="66fe8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66fe8-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="66fe8-112">Bu komut, SYNAPSE Analytics Spark oturumunun zaman aşımını belirtilen Livy KIMLIĞIYLE sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="66fe8-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="66fe8-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="66fe8-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="66fe8-114">Bu komut, SYNAPSE Analytics Spark oturumunun zaman aşımını belirtilen Livy ile ardışık düzen ile sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="66fe8-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="66fe8-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="66fe8-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="66fe8-116">Bu komut, SYNAPSE Analytics Spark oturumunun zaman aşımını belirtilen Livy ile ardışık düzen ile sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="66fe8-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="66fe8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66fe8-117">PARAMETERS</span></span>

### <span data-ttu-id="66fe8-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="66fe8-118">-AsJob</span></span>
<span data-ttu-id="66fe8-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="66fe8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66fe8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fe8-120">-DefaultProfile</span></span>
<span data-ttu-id="66fe8-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66fe8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fe8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66fe8-122">-InputObject</span></span>
<span data-ttu-id="66fe8-123">Spark oturum giriş nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="66fe8-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66fe8-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="66fe8-124">-LivyId</span></span>
<span data-ttu-id="66fe8-125">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="66fe8-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fe8-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66fe8-126">-PassThru</span></span>
<span data-ttu-id="66fe8-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="66fe8-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="66fe8-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="66fe8-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="66fe8-129">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="66fe8-129">-SparkPoolName</span></span>
<span data-ttu-id="66fe8-130">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="66fe8-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fe8-131">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="66fe8-131">-SparkPoolObject</span></span>
<span data-ttu-id="66fe8-132">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="66fe8-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66fe8-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="66fe8-133">-WorkspaceName</span></span>
<span data-ttu-id="66fe8-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="66fe8-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fe8-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="66fe8-135">-Confirm</span></span>
<span data-ttu-id="66fe8-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66fe8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fe8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fe8-137">-WhatIf</span></span>
<span data-ttu-id="66fe8-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66fe8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fe8-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66fe8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fe8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fe8-140">CommonParameters</span></span>
<span data-ttu-id="66fe8-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66fe8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fe8-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66fe8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fe8-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66fe8-143">INPUTS</span></span>

### <span data-ttu-id="66fe8-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="66fe8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="66fe8-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="66fe8-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="66fe8-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66fe8-146">OUTPUTS</span></span>

### <span data-ttu-id="66fe8-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66fe8-147">System.Boolean</span></span>

## <span data-ttu-id="66fe8-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66fe8-148">NOTES</span></span>

## <span data-ttu-id="66fe8-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66fe8-149">RELATED LINKS</span></span>
