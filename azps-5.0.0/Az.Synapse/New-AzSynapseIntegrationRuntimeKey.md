---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277934"
---
# <span data-ttu-id="ea453-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="ea453-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="ea453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea453-102">SYNOPSIS</span></span>
<span data-ttu-id="ea453-103">Self-hosted Integration Runtime anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ea453-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="ea453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea453-104">SYNTAX</span></span>

### <span data-ttu-id="ea453-105">NewByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea453-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea453-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea453-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea453-107">Newbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ea453-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea453-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea453-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea453-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea453-109">DESCRIPTION</span></span>
<span data-ttu-id="ea453-110">**New-AzSynapseIntegrationRuntimeKey** cmdlet 'ı ' KeyName ' parametresiyle belirtilen anahtar adıyla tümleştirme çalışma zamanı anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea453-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="ea453-111">Önceki anahtar geçersiz olur.</span><span class="sxs-lookup"><span data-stu-id="ea453-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="ea453-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea453-112">EXAMPLES</span></span>

### <span data-ttu-id="ea453-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea453-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="ea453-114">' Test-Selfhost-IR ' adlı tümleştirme çalışma zamanı için cmdlet ' authKey2 ' anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea453-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ea453-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea453-115">PARAMETERS</span></span>

### <span data-ttu-id="ea453-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea453-116">-DefaultProfile</span></span>
<span data-ttu-id="ea453-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea453-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea453-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ea453-118">-Force</span></span>
<span data-ttu-id="ea453-119">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="ea453-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea453-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea453-120">-InputObject</span></span>
<span data-ttu-id="ea453-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ea453-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-122">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="ea453-122">-KeyName</span></span>
<span data-ttu-id="ea453-123">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı adı.</span><span class="sxs-lookup"><span data-stu-id="ea453-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea453-124">-Name</span></span>
<span data-ttu-id="ea453-125">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="ea453-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea453-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea453-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea453-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ea453-128">-ResourceId</span></span>
<span data-ttu-id="ea453-129">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ea453-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ea453-130">-WorkspaceName</span></span>
<span data-ttu-id="ea453-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ea453-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-132">-</span><span class="sxs-lookup"><span data-stu-id="ea453-132">-WorkspaceObject</span></span>
<span data-ttu-id="ea453-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ea453-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea453-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea453-134">-Confirm</span></span>
<span data-ttu-id="ea453-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea453-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea453-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea453-136">-WhatIf</span></span>
<span data-ttu-id="ea453-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea453-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea453-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea453-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea453-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea453-139">CommonParameters</span></span>
<span data-ttu-id="ea453-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea453-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea453-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea453-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea453-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea453-142">INPUTS</span></span>

### <span data-ttu-id="ea453-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea453-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ea453-144">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="ea453-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ea453-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea453-145">OUTPUTS</span></span>

### <span data-ttu-id="ea453-146">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="ea453-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="ea453-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea453-147">NOTES</span></span>

## <span data-ttu-id="ea453-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea453-148">RELATED LINKS</span></span>
