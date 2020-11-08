---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279282"
---
# <span data-ttu-id="164f7-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="164f7-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="164f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="164f7-102">SYNOPSIS</span></span>
<span data-ttu-id="164f7-103">SYNAPSE Analytics Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="164f7-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="164f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="164f7-104">SYNTAX</span></span>

### <span data-ttu-id="164f7-105">Stopmini Ifade (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="164f7-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="164f7-106">Stopmini Statebyıdfromparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="164f7-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="164f7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="164f7-107">DESCRIPTION</span></span>
<span data-ttu-id="164f7-108">**Stop-AzSynapseSparkStatement** cmdlet 'ı bir Synapse Analytics Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="164f7-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="164f7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="164f7-109">EXAMPLES</span></span>

### <span data-ttu-id="164f7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="164f7-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="164f7-111">Bu komut, belirtilen Livy KIMLIĞIYLE Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="164f7-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="164f7-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="164f7-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="164f7-113">Bu komut, ardışık düzen aracılığıyla belirtilen Livy KIMLIĞI ile Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="164f7-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="164f7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="164f7-114">PARAMETERS</span></span>

### <span data-ttu-id="164f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164f7-115">-DefaultProfile</span></span>
<span data-ttu-id="164f7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="164f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="164f7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="164f7-117">-Force</span></span>
<span data-ttu-id="164f7-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="164f7-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="164f7-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="164f7-119">-LivyId</span></span>
<span data-ttu-id="164f7-120">Spark deyiminin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="164f7-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="164f7-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="164f7-121">-PassThru</span></span>
<span data-ttu-id="164f7-122">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="164f7-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="164f7-123">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="164f7-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="164f7-124">-SessionID</span><span class="sxs-lookup"><span data-stu-id="164f7-124">-SessionId</span></span>
<span data-ttu-id="164f7-125">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="164f7-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="164f7-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="164f7-126">-SessionObject</span></span>
<span data-ttu-id="164f7-127">Spark oturum giriş nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="164f7-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="164f7-128">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="164f7-128">-SparkPoolName</span></span>
<span data-ttu-id="164f7-129">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="164f7-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="164f7-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="164f7-130">-WorkspaceName</span></span>
<span data-ttu-id="164f7-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="164f7-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="164f7-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="164f7-132">-Confirm</span></span>
<span data-ttu-id="164f7-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="164f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164f7-134">-WhatIf</span></span>
<span data-ttu-id="164f7-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="164f7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="164f7-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="164f7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="164f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164f7-137">CommonParameters</span></span>
<span data-ttu-id="164f7-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="164f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164f7-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="164f7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164f7-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="164f7-140">INPUTS</span></span>

### <span data-ttu-id="164f7-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="164f7-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="164f7-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="164f7-142">OUTPUTS</span></span>

### <span data-ttu-id="164f7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="164f7-143">System.Boolean</span></span>

## <span data-ttu-id="164f7-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="164f7-144">NOTES</span></span>

## <span data-ttu-id="164f7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="164f7-145">RELATED LINKS</span></span>
