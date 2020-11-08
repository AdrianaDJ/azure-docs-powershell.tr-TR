---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107456"
---
# <span data-ttu-id="a5a2f-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a5a2f-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="a5a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a2f-103">SYNAPSE Analytics SQL veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a5a2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5a2f-104">SYNTAX</span></span>

### <span data-ttu-id="a5a2f-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5a2f-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a2f-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a2f-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a2f-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a2f-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a2f-108">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a5a2f-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a2f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5a2f-109">DESCRIPTION</span></span>
<span data-ttu-id="a5a2f-110">**Update-AzSynapseSqlDatabase** cmdlet 'ı bir Azure SYNAPSE Analytics SQL veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a5a2f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5a2f-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a2f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5a2f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="a5a2f-113">Bu komut, bir Azure SYNAPSE Analytics SQL veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a5a2f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="a5a2f-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="a5a2f-115">-AsJob</span></span>
<span data-ttu-id="a5a2f-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a5a2f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5a2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a2f-117">-DefaultProfile</span></span>
<span data-ttu-id="a5a2f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a2f-119">-InputObject</span></span>
<span data-ttu-id="a5a2f-120">Genellikle ardışık düzen aracılığıyla iletilen SQL veritabanı giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a5a2f-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="a5a2f-122">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5a2f-123">-Name</span></span>
<span data-ttu-id="a5a2f-124">SYNAPSE SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a5a2f-125">-PassThru</span></span>
<span data-ttu-id="a5a2f-126">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a5a2f-127">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a5a2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5a2f-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5a2f-130">-ResourceId</span></span>
<span data-ttu-id="a5a2f-131">SYNAPSE SQL veritabanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a5a2f-132">-Tag</span></span>
<span data-ttu-id="a5a2f-133">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a5a2f-134">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a5a2f-134">-WorkspaceName</span></span>
<span data-ttu-id="a5a2f-135">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-136">-</span><span class="sxs-lookup"><span data-stu-id="a5a2f-136">-WorkspaceObject</span></span>
<span data-ttu-id="a5a2f-137">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5a2f-138">-Confirm</span></span>
<span data-ttu-id="a5a2f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a2f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a2f-140">-WhatIf</span></span>
<span data-ttu-id="a5a2f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a2f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a2f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a2f-143">CommonParameters</span></span>
<span data-ttu-id="a5a2f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a2f-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5a2f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a2f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5a2f-146">INPUTS</span></span>

### <span data-ttu-id="a5a2f-147">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5a2f-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a5a2f-148">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a5a2f-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="a5a2f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5a2f-149">OUTPUTS</span></span>

### <span data-ttu-id="a5a2f-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a5a2f-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="a5a2f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5a2f-151">NOTES</span></span>

## <span data-ttu-id="a5a2f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5a2f-152">RELATED LINKS</span></span>
