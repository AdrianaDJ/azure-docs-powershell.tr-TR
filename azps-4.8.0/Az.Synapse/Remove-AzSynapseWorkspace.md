---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268941"
---
# <span data-ttu-id="62a9a-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="62a9a-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="62a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="62a9a-103">SYNAPSE Analytics çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="62a9a-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="62a9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62a9a-104">SYNTAX</span></span>

### <span data-ttu-id="62a9a-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62a9a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a9a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a9a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a9a-107">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="62a9a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a9a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="62a9a-108">DESCRIPTION</span></span>
<span data-ttu-id="62a9a-109">**Remove-AzSynapseWorkspace** cmdlet 'ı bir Azure SYNAPSE Analytics çalışma alanını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="62a9a-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="62a9a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62a9a-110">EXAMPLES</span></span>

### <span data-ttu-id="62a9a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62a9a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="62a9a-112">Bu komut bir Azure SYNAPSE Analytics çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="62a9a-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="62a9a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="62a9a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="62a9a-114">Bu komut bir Azure SYNAPSE Analytics çalışma alanını ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="62a9a-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="62a9a-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="62a9a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="62a9a-116">Bu komut, belirtilen kaynak KIMLIĞIYLE ardışık düzen aracılığıyla Azure SYNAPSE Analytics çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="62a9a-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="62a9a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62a9a-117">PARAMETERS</span></span>

### <span data-ttu-id="62a9a-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="62a9a-118">-AsJob</span></span>
<span data-ttu-id="62a9a-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="62a9a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62a9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a9a-120">-DefaultProfile</span></span>
<span data-ttu-id="62a9a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62a9a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a9a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62a9a-122">-InputObject</span></span>
<span data-ttu-id="62a9a-123">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="62a9a-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62a9a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="62a9a-124">-Name</span></span>
<span data-ttu-id="62a9a-125">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="62a9a-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a9a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="62a9a-126">-PassThru</span></span>
<span data-ttu-id="62a9a-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="62a9a-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="62a9a-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="62a9a-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="62a9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="62a9a-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="62a9a-130">Resource group name.</span></span>

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

### <span data-ttu-id="62a9a-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="62a9a-131">-ResourceId</span></span>
<span data-ttu-id="62a9a-132">SYNAPSE çalışma alanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="62a9a-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a9a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="62a9a-133">-Confirm</span></span>
<span data-ttu-id="62a9a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62a9a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a9a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a9a-135">-WhatIf</span></span>
<span data-ttu-id="62a9a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62a9a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a9a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62a9a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a9a-138">CommonParameters</span></span>
<span data-ttu-id="62a9a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62a9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a9a-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62a9a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a9a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62a9a-141">INPUTS</span></span>

### <span data-ttu-id="62a9a-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="62a9a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="62a9a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62a9a-143">OUTPUTS</span></span>

### <span data-ttu-id="62a9a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62a9a-144">System.Boolean</span></span>

## <span data-ttu-id="62a9a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62a9a-145">NOTES</span></span>

## <span data-ttu-id="62a9a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62a9a-146">RELATED LINKS</span></span>
