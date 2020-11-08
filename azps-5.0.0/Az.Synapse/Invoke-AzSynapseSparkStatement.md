---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276609"
---
# <span data-ttu-id="bbf1a-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="bbf1a-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="bbf1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf1a-103">SYNAPSE çözümleme Spark deyimini çağırır.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbf1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbf1a-104">SYNTAX</span></span>

### <span data-ttu-id="bbf1a-105">Runmini Ifade değeri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbf1a-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf1a-106">Runmini Ifade ifadesi</span><span class="sxs-lookup"><span data-stu-id="bbf1a-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf1a-107">Runmini ifade Durumüpdınputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="bbf1a-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf1a-108">Runmini Ifade Statebycodepathandınputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="bbf1a-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbf1a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbf1a-109">DESCRIPTION</span></span>
<span data-ttu-id="bbf1a-110">**Invoke-AzSynapseSparkStatement** cmdlet 'ı bir Synapse Analytics Spark deyimini çağırır.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbf1a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbf1a-111">EXAMPLES</span></span>

### <span data-ttu-id="bbf1a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bbf1a-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="bbf1a-113">Bu komutlar, bir Spark oturumu başlatır ve ardından satır içi Spark deyimini ardışık düzen aracılığıyla başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="bbf1a-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bbf1a-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="bbf1a-115">Bu komutlar, bir Spark oturumu başlatır ve ardından satır içi Spark deyimini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="bbf1a-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bbf1a-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="bbf1a-117">Bu komutlar, bir Spark oturumu başlatır ve bir dosyada Spark deyimlerini çağırır.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="bbf1a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbf1a-118">PARAMETERS</span></span>

### <span data-ttu-id="bbf1a-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="bbf1a-119">-AsJob</span></span>
<span data-ttu-id="bbf1a-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bbf1a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbf1a-121">-Kod</span><span class="sxs-lookup"><span data-stu-id="bbf1a-121">-Code</span></span>
<span data-ttu-id="bbf1a-122">Yürütme kodu.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf1a-123">-DefaultProfile</span></span>
<span data-ttu-id="bbf1a-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf1a-125">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="bbf1a-125">-FilePath</span></span>
<span data-ttu-id="bbf1a-126">Yürütme kodunu içeren yerel bir dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-127">-Dil</span><span class="sxs-lookup"><span data-stu-id="bbf1a-127">-Language</span></span>
<span data-ttu-id="bbf1a-128">Yürütme kodunun dili.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-129">-Response</span><span class="sxs-lookup"><span data-stu-id="bbf1a-129">-Response</span></span>
<span data-ttu-id="bbf1a-130">Tam yanıtın döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="bbf1a-131">-SessionID</span><span class="sxs-lookup"><span data-stu-id="bbf1a-131">-SessionId</span></span>
<span data-ttu-id="bbf1a-132">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="bbf1a-133">-SessionObject</span></span>
<span data-ttu-id="bbf1a-134">Spark oturum giriş nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-135">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="bbf1a-135">-SparkPoolName</span></span>
<span data-ttu-id="bbf1a-136">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-137">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bbf1a-137">-WorkspaceName</span></span>
<span data-ttu-id="bbf1a-138">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf1a-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbf1a-139">-Confirm</span></span>
<span data-ttu-id="bbf1a-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf1a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf1a-141">-WhatIf</span></span>
<span data-ttu-id="bbf1a-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbf1a-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf1a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf1a-144">CommonParameters</span></span>
<span data-ttu-id="bbf1a-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf1a-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbf1a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf1a-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbf1a-147">INPUTS</span></span>

### <span data-ttu-id="bbf1a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf1a-148">System.String</span></span>

### <span data-ttu-id="bbf1a-149">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="bbf1a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="bbf1a-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbf1a-150">OUTPUTS</span></span>

### <span data-ttu-id="bbf1a-151">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="bbf1a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="bbf1a-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbf1a-152">NOTES</span></span>

## <span data-ttu-id="bbf1a-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbf1a-153">RELATED LINKS</span></span>
