---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324157"
---
# <span data-ttu-id="6e3ee-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6e3ee-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="6e3ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3ee-103">SYNAPSE Analizi Spark havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6e3ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e3ee-104">SYNTAX</span></span>

### <span data-ttu-id="6e3ee-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e3ee-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e3ee-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3ee-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e3ee-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6e3ee-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e3ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="6e3ee-109">**Get-AzSynapseSparkPool** cmdlet 'ı bir Azure SYNAPSE Analytics Spark havuzu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6e3ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e3ee-110">EXAMPLES</span></span>

### <span data-ttu-id="6e3ee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6e3ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6e3ee-112">Bu komut, çalışma alanı altındaki tüm Spark havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="6e3ee-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6e3ee-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="6e3ee-114">Bu komut, çalışma alanı adı Contosomini havuz altında bulunan Spark havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="6e3ee-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6e3ee-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="6e3ee-116">Bu komut, ardışık düzen aracılığıyla çalışma alanı altındaki tüm Spark havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="6e3ee-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="6e3ee-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="6e3ee-118">Bu komut, belirtilen kaynak KIMLIĞIYLE Spark havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="6e3ee-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e3ee-119">PARAMETERS</span></span>

### <span data-ttu-id="6e3ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3ee-120">-DefaultProfile</span></span>
<span data-ttu-id="6e3ee-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3ee-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e3ee-122">-Name</span></span>
<span data-ttu-id="6e3ee-123">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e3ee-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ee-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6e3ee-126">-ResourceId</span></span>
<span data-ttu-id="6e3ee-127">SYNAPSE Spark havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ee-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6e3ee-128">-WorkspaceName</span></span>
<span data-ttu-id="6e3ee-129">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ee-130">-</span><span class="sxs-lookup"><span data-stu-id="6e3ee-130">-WorkspaceObject</span></span>
<span data-ttu-id="6e3ee-131">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3ee-132">CommonParameters</span></span>
<span data-ttu-id="6e3ee-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3ee-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e3ee-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3ee-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e3ee-135">INPUTS</span></span>

### <span data-ttu-id="6e3ee-136">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e3ee-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6e3ee-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e3ee-137">OUTPUTS</span></span>

### <span data-ttu-id="6e3ee-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6e3ee-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6e3ee-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e3ee-139">NOTES</span></span>

## <span data-ttu-id="6e3ee-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e3ee-140">RELATED LINKS</span></span>
