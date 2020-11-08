---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107465"
---
# <span data-ttu-id="68988-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="68988-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="68988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68988-102">SYNOPSIS</span></span>
<span data-ttu-id="68988-103">SYNAPSE Analytics Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="68988-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="68988-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68988-104">SYNTAX</span></span>

### <span data-ttu-id="68988-105">Stopmini Ifade (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68988-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68988-106">Stopmini Statebyıdfromparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="68988-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68988-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="68988-107">DESCRIPTION</span></span>
<span data-ttu-id="68988-108">**Stop-AzSynapseSparkStatement** cmdlet 'ı bir Synapse Analytics Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="68988-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="68988-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68988-109">EXAMPLES</span></span>

### <span data-ttu-id="68988-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68988-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="68988-111">Bu komut, belirtilen Livy KIMLIĞIYLE Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="68988-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="68988-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="68988-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="68988-113">Bu komut, ardışık düzen aracılığıyla belirtilen Livy KIMLIĞI ile Spark deyimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="68988-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="68988-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68988-114">PARAMETERS</span></span>

### <span data-ttu-id="68988-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68988-115">-DefaultProfile</span></span>
<span data-ttu-id="68988-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68988-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68988-117">-Force</span><span class="sxs-lookup"><span data-stu-id="68988-117">-Force</span></span>
<span data-ttu-id="68988-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="68988-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68988-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="68988-119">-LivyId</span></span>
<span data-ttu-id="68988-120">Spark deyiminin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="68988-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="68988-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="68988-121">-PassThru</span></span>
<span data-ttu-id="68988-122">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="68988-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="68988-123">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="68988-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="68988-124">-SessionID</span><span class="sxs-lookup"><span data-stu-id="68988-124">-SessionId</span></span>
<span data-ttu-id="68988-125">Spark oturumunun tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="68988-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="68988-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="68988-126">-SessionObject</span></span>
<span data-ttu-id="68988-127">Spark oturum giriş nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="68988-127">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68988-128">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="68988-128">-SparkPoolName</span></span>
<span data-ttu-id="68988-129">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="68988-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="68988-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="68988-130">-WorkspaceName</span></span>
<span data-ttu-id="68988-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="68988-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68988-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="68988-132">-Confirm</span></span>
<span data-ttu-id="68988-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68988-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68988-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68988-134">-WhatIf</span></span>
<span data-ttu-id="68988-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68988-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68988-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68988-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68988-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68988-137">CommonParameters</span></span>
<span data-ttu-id="68988-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68988-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68988-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68988-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68988-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68988-140">INPUTS</span></span>

### <span data-ttu-id="68988-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="68988-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="68988-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68988-142">OUTPUTS</span></span>

### <span data-ttu-id="68988-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68988-143">System.Boolean</span></span>

## <span data-ttu-id="68988-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68988-144">NOTES</span></span>

## <span data-ttu-id="68988-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68988-145">RELATED LINKS</span></span>
