---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277136"
---
# <span data-ttu-id="94452-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94452-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="94452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94452-102">SYNOPSIS</span></span>
<span data-ttu-id="94452-103">SYNAPSE Analytics SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="94452-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="94452-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94452-104">SYNTAX</span></span>

### <span data-ttu-id="94452-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94452-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94452-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94452-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94452-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94452-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94452-108">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="94452-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94452-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="94452-109">DESCRIPTION</span></span>
<span data-ttu-id="94452-110">**Remove-AzSynapseSqlPool** cmdlet 'i, bir Azure SYNAPSE Analytics SQL veritabanını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="94452-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="94452-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94452-111">EXAMPLES</span></span>

### <span data-ttu-id="94452-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94452-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="94452-113">Bu komut bir Azure SYNAPSE Analytics SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="94452-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="94452-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="94452-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="94452-115">Bu komut bir Azure SYNAPSE Analytics SQL veritabanını ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="94452-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="94452-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="94452-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="94452-117">Bu komut bir Azure SYNAPSE Analytics SQL veritabanını ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="94452-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="94452-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="94452-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="94452-119">Bu komut belirtilen kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="94452-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="94452-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94452-120">PARAMETERS</span></span>

### <span data-ttu-id="94452-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="94452-121">-AsJob</span></span>
<span data-ttu-id="94452-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="94452-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94452-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94452-123">-DefaultProfile</span></span>
<span data-ttu-id="94452-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94452-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94452-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94452-125">-InputObject</span></span>
<span data-ttu-id="94452-126">Genellikle ardışık düzen aracılığıyla iletilen SQL veritabanı giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="94452-126">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94452-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="94452-127">-Name</span></span>
<span data-ttu-id="94452-128">SYNAPSE SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="94452-128">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94452-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94452-129">-PassThru</span></span>
<span data-ttu-id="94452-130">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="94452-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94452-131">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="94452-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="94452-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94452-132">-ResourceGroupName</span></span>
<span data-ttu-id="94452-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="94452-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94452-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="94452-134">-ResourceId</span></span>
<span data-ttu-id="94452-135">SYNAPSE SQL veritabanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="94452-135">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94452-136">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="94452-136">-WorkspaceName</span></span>
<span data-ttu-id="94452-137">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="94452-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="94452-138">-</span><span class="sxs-lookup"><span data-stu-id="94452-138">-WorkspaceObject</span></span>
<span data-ttu-id="94452-139">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="94452-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94452-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="94452-140">-Confirm</span></span>
<span data-ttu-id="94452-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94452-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94452-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94452-142">-WhatIf</span></span>
<span data-ttu-id="94452-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94452-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94452-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94452-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94452-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94452-145">CommonParameters</span></span>
<span data-ttu-id="94452-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94452-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94452-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94452-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94452-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94452-148">INPUTS</span></span>

### <span data-ttu-id="94452-149">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="94452-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="94452-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94452-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="94452-151">System. String</span><span class="sxs-lookup"><span data-stu-id="94452-151">System.String</span></span>

## <span data-ttu-id="94452-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94452-152">OUTPUTS</span></span>

### <span data-ttu-id="94452-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94452-153">System.Boolean</span></span>

## <span data-ttu-id="94452-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94452-154">NOTES</span></span>

## <span data-ttu-id="94452-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94452-155">RELATED LINKS</span></span>
