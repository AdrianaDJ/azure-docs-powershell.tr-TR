---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276603"
---
# <span data-ttu-id="05747-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="05747-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="05747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05747-102">SYNOPSIS</span></span>
<span data-ttu-id="05747-103">SYNAPSE Analytics güvenlik duvarı kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="05747-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="05747-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05747-104">SYNTAX</span></span>

### <span data-ttu-id="05747-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05747-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05747-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05747-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05747-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05747-107">DESCRIPTION</span></span>
<span data-ttu-id="05747-108">**Remove-AzSynapseFirewallRule** cmdlet 'ı bir Azure SYNAPSE Analytics güvenlik duvarı kuralını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="05747-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="05747-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05747-109">EXAMPLES</span></span>

### <span data-ttu-id="05747-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05747-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="05747-111">Bu komut ContosoFirewallRule adındaki güvenlik duvarı kuralını çalışma alanı ContosoFirewallRule adıyla siler.</span><span class="sxs-lookup"><span data-stu-id="05747-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="05747-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="05747-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="05747-113">Bu komut, ContosoFirewallRule adındaki güvenlik duvarı kuralını ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="05747-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="05747-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05747-114">PARAMETERS</span></span>

### <span data-ttu-id="05747-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="05747-115">-AsJob</span></span>
<span data-ttu-id="05747-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="05747-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05747-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05747-117">-DefaultProfile</span></span>
<span data-ttu-id="05747-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05747-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05747-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="05747-119">-Name</span></span>
<span data-ttu-id="05747-120">Çalışma alanı için firerduvar kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="05747-120">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05747-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="05747-121">-PassThru</span></span>
<span data-ttu-id="05747-122">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="05747-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="05747-123">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="05747-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="05747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05747-124">-ResourceGroupName</span></span>
<span data-ttu-id="05747-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="05747-125">Resource group name.</span></span>

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

### <span data-ttu-id="05747-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="05747-126">-WorkspaceName</span></span>
<span data-ttu-id="05747-127">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="05747-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="05747-128">-</span><span class="sxs-lookup"><span data-stu-id="05747-128">-WorkspaceObject</span></span>
<span data-ttu-id="05747-129">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="05747-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="05747-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="05747-130">-Confirm</span></span>
<span data-ttu-id="05747-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05747-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05747-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05747-132">-WhatIf</span></span>
<span data-ttu-id="05747-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05747-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05747-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05747-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05747-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05747-135">CommonParameters</span></span>
<span data-ttu-id="05747-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05747-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05747-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05747-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05747-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05747-138">INPUTS</span></span>

### <span data-ttu-id="05747-139">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="05747-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="05747-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05747-140">OUTPUTS</span></span>

### <span data-ttu-id="05747-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05747-141">System.Boolean</span></span>

## <span data-ttu-id="05747-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05747-142">NOTES</span></span>

## <span data-ttu-id="05747-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05747-143">RELATED LINKS</span></span>
