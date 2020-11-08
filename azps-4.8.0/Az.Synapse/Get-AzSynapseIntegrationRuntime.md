---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273776"
---
# <span data-ttu-id="dcbc0-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dcbc0-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="dcbc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbc0-103">Tümleştirme çalışma zamanı kaynakları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="dcbc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcbc0-104">SYNTAX</span></span>

### <span data-ttu-id="dcbc0-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcbc0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbc0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc0-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dcbc0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcbc0-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbc0-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbc0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcbc0-109">DESCRIPTION</span></span>
<span data-ttu-id="dcbc0-110">**Get-AzSynapseIntegrationRuntime** cmdlet 'i, çalışma alanındaki tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="dcbc0-111">Bir tümleştirme çalışma zamanının adını belirtirseniz, bu cmdlet Bu tümleştirme çalışma zamanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="dcbc0-112">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="dcbc0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcbc0-113">EXAMPLES</span></span>

### <span data-ttu-id="dcbc0-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcbc0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="dcbc0-115">ContosoWorkspace adlı çalışma alanındaki tüm tümleştirme çalışma zamanlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dcbc0-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dcbc0-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="dcbc0-117">Bu komut, ContosoWorkspace adlı çalışma alanındaki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dcbc0-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="dcbc0-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="dcbc0-119">Bu komut, ContosoWorkspace adlı çalışma alanındaki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ayrıntı durumunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="dcbc0-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcbc0-120">PARAMETERS</span></span>

### <span data-ttu-id="dcbc0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbc0-121">-DefaultProfile</span></span>
<span data-ttu-id="dcbc0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcbc0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcbc0-123">-InputObject</span></span>
<span data-ttu-id="dcbc0-124">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcbc0-125">-Name</span></span>
<span data-ttu-id="dcbc0-126">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbc0-127">-ResourceGroupName</span></span>
<span data-ttu-id="dcbc0-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-128">Resource group name.</span></span>

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

### <span data-ttu-id="dcbc0-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dcbc0-129">-ResourceId</span></span>
<span data-ttu-id="dcbc0-130">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="dcbc0-131">-Durum</span><span class="sxs-lookup"><span data-stu-id="dcbc0-131">-Status</span></span>
<span data-ttu-id="dcbc0-132">Tümleştirme çalışma zamanı ayrıntı durumu.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="dcbc0-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="dcbc0-133">-WorkspaceName</span></span>
<span data-ttu-id="dcbc0-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dcbc0-135">-</span><span class="sxs-lookup"><span data-stu-id="dcbc0-135">-WorkspaceObject</span></span>
<span data-ttu-id="dcbc0-136">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcbc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbc0-137">CommonParameters</span></span>
<span data-ttu-id="dcbc0-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbc0-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcbc0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbc0-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcbc0-140">INPUTS</span></span>

### <span data-ttu-id="dcbc0-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcbc0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dcbc0-142">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="dcbc0-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dcbc0-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcbc0-143">OUTPUTS</span></span>

### <span data-ttu-id="dcbc0-144">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="dcbc0-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dcbc0-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcbc0-145">NOTES</span></span>

## <span data-ttu-id="dcbc0-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcbc0-146">RELATED LINKS</span></span>
