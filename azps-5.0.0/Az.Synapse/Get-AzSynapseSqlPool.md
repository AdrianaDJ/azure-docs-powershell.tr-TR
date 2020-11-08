---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276610"
---
# <span data-ttu-id="a1adf-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a1adf-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a1adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1adf-102">SYNOPSIS</span></span>
<span data-ttu-id="a1adf-103">SYNAPSE Analytics SQL havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a1adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1adf-104">SYNTAX</span></span>

### <span data-ttu-id="a1adf-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1adf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1adf-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1adf-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1adf-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a1adf-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1adf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1adf-108">DESCRIPTION</span></span>
<span data-ttu-id="a1adf-109">**Get-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a1adf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1adf-110">EXAMPLES</span></span>

### <span data-ttu-id="a1adf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1adf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a1adf-112">Bu komut, çalışma alanı altındaki tüm SQL havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="a1adf-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a1adf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a1adf-114">Bu komut, SQL havuzunu çalışma alanı 'nın altındaki ContosoSqlPool ile alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="a1adf-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a1adf-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="a1adf-116">Bu komut, ardışık düzen aracılığıyla bir çalışma alanı altındaki tüm SQL havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="a1adf-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a1adf-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="a1adf-118">Bu komut, belirtilen kaynak KIMLIĞIYLE SQL havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="a1adf-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="a1adf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1adf-119">PARAMETERS</span></span>

### <span data-ttu-id="a1adf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1adf-120">-DefaultProfile</span></span>
<span data-ttu-id="a1adf-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1adf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1adf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1adf-122">-Name</span></span>
<span data-ttu-id="a1adf-123">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="a1adf-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1adf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1adf-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1adf-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a1adf-125">Resource group name.</span></span>

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

### <span data-ttu-id="a1adf-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a1adf-126">-ResourceId</span></span>
<span data-ttu-id="a1adf-127">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a1adf-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a1adf-128">-Version</span><span class="sxs-lookup"><span data-stu-id="a1adf-128">-Version</span></span>
<span data-ttu-id="a1adf-129">[Bu özellik, başlangıçta yalnızca belirli aboneliklerde erişilebilen sınırlı bir önizlemede.] SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="a1adf-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="a1adf-130">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="a1adf-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1adf-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a1adf-131">-WorkspaceName</span></span>
<span data-ttu-id="a1adf-132">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="a1adf-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1adf-133">-</span><span class="sxs-lookup"><span data-stu-id="a1adf-133">-WorkspaceObject</span></span>
<span data-ttu-id="a1adf-134">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="a1adf-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1adf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1adf-135">CommonParameters</span></span>
<span data-ttu-id="a1adf-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1adf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1adf-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1adf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1adf-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1adf-138">INPUTS</span></span>

### <span data-ttu-id="a1adf-139">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1adf-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a1adf-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1adf-140">OUTPUTS</span></span>

### <span data-ttu-id="a1adf-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a1adf-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a1adf-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1adf-142">NOTES</span></span>

## <span data-ttu-id="a1adf-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1adf-143">RELATED LINKS</span></span>
