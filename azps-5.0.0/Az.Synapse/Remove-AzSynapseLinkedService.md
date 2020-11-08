---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277913"
---
# <span data-ttu-id="13d7e-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="13d7e-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="13d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="13d7e-103">Bağlantılı hizmeti çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13d7e-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="13d7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13d7e-104">SYNTAX</span></span>

### <span data-ttu-id="13d7e-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13d7e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d7e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="13d7e-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13d7e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="13d7e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13d7e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13d7e-108">DESCRIPTION</span></span>
<span data-ttu-id="13d7e-109">**Remove-AzSynapseLinkedService** cmdlet 'i çalışma alanından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13d7e-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="13d7e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="13d7e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13d7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="13d7e-112">Bu komut, ContosoLinkedService adındaki bağlantılı hizmeti ContosoWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13d7e-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="13d7e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="13d7e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="13d7e-114">Bu komut, ContosoLinkedService adındaki bağlantılı hizmeti Contosoçalışma alanı adlı çalışma alanından ardışık düzen aracılığıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13d7e-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="13d7e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="13d7e-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="13d7e-116">Bu komut, ContosoLinkedService adındaki bağlantılı hizmeti Contosoçalışma alanı adlı çalışma alanından ardışık düzen aracılığıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13d7e-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="13d7e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13d7e-117">PARAMETERS</span></span>

### <span data-ttu-id="13d7e-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="13d7e-118">-AsJob</span></span>
<span data-ttu-id="13d7e-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="13d7e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13d7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d7e-120">-DefaultProfile</span></span>
<span data-ttu-id="13d7e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13d7e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13d7e-122">-InputObject</span></span>
<span data-ttu-id="13d7e-123">Bağlantılı hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="13d7e-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d7e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="13d7e-124">-Name</span></span>
<span data-ttu-id="13d7e-125">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="13d7e-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d7e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="13d7e-126">-PassThru</span></span>
<span data-ttu-id="13d7e-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="13d7e-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="13d7e-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="13d7e-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="13d7e-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="13d7e-129">-WorkspaceName</span></span>
<span data-ttu-id="13d7e-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="13d7e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d7e-131">-</span><span class="sxs-lookup"><span data-stu-id="13d7e-131">-WorkspaceObject</span></span>
<span data-ttu-id="13d7e-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="13d7e-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d7e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="13d7e-133">-Confirm</span></span>
<span data-ttu-id="13d7e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13d7e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13d7e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d7e-135">-WhatIf</span></span>
<span data-ttu-id="13d7e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13d7e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13d7e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13d7e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13d7e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d7e-138">CommonParameters</span></span>
<span data-ttu-id="13d7e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13d7e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d7e-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13d7e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d7e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13d7e-141">INPUTS</span></span>

### <span data-ttu-id="13d7e-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="13d7e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="13d7e-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="13d7e-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="13d7e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13d7e-144">OUTPUTS</span></span>

### <span data-ttu-id="13d7e-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="13d7e-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="13d7e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13d7e-146">NOTES</span></span>

## <span data-ttu-id="13d7e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13d7e-147">RELATED LINKS</span></span>
