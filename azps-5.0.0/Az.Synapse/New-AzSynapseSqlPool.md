---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279294"
---
# <span data-ttu-id="7b420-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7b420-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7b420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b420-102">SYNOPSIS</span></span>
<span data-ttu-id="7b420-103">SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b420-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7b420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b420-104">SYNTAX</span></span>

### <span data-ttu-id="7b420-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7b420-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b420-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b420-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b420-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b420-107">DESCRIPTION</span></span>
<span data-ttu-id="7b420-108">**New-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b420-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7b420-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b420-109">EXAMPLES</span></span>

### <span data-ttu-id="7b420-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b420-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="7b420-111">Bu komut, bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b420-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7b420-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b420-112">PARAMETERS</span></span>

### <span data-ttu-id="7b420-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7b420-113">-AsJob</span></span>
<span data-ttu-id="7b420-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7b420-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b420-115">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="7b420-115">-Collation</span></span>
<span data-ttu-id="7b420-116">Harmanlama, verileri sıralayan ve karşılaştıran kuralları tanımlar ve SQL havuzu oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="7b420-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="7b420-117">Varsayılan alfabe düzeni SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="7b420-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="7b420-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b420-118">-DefaultProfile</span></span>
<span data-ttu-id="7b420-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b420-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b420-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b420-120">-Name</span></span>
<span data-ttu-id="7b420-121">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="7b420-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7b420-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="7b420-122">-PerformanceLevel</span></span>
<span data-ttu-id="7b420-123">SQL havuzuna atanacak SQL hizmet katmanı ve performans düzeyi.</span><span class="sxs-lookup"><span data-stu-id="7b420-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="7b420-124">Örneğin, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="7b420-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="7b420-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b420-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b420-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7b420-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b420-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7b420-127">-Tag</span></span>
<span data-ttu-id="7b420-128">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="7b420-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="7b420-129">-Version</span><span class="sxs-lookup"><span data-stu-id="7b420-129">-Version</span></span>
<span data-ttu-id="7b420-130">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="7b420-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="7b420-131">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="7b420-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="7b420-132">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7b420-132">-WorkspaceName</span></span>
<span data-ttu-id="7b420-133">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="7b420-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7b420-134">-</span><span class="sxs-lookup"><span data-stu-id="7b420-134">-WorkspaceObject</span></span>
<span data-ttu-id="7b420-135">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="7b420-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b420-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b420-136">-Confirm</span></span>
<span data-ttu-id="7b420-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b420-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b420-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b420-138">-WhatIf</span></span>
<span data-ttu-id="7b420-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b420-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b420-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b420-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b420-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b420-141">CommonParameters</span></span>
<span data-ttu-id="7b420-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b420-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b420-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7b420-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b420-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b420-144">INPUTS</span></span>

### <span data-ttu-id="7b420-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7b420-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7b420-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b420-146">OUTPUTS</span></span>

### <span data-ttu-id="7b420-147">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7b420-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7b420-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b420-148">NOTES</span></span>

## <span data-ttu-id="7b420-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b420-149">RELATED LINKS</span></span>
