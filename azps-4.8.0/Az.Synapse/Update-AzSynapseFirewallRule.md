---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107458"
---
# <span data-ttu-id="dab49-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dab49-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="dab49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab49-102">SYNOPSIS</span></span>
<span data-ttu-id="dab49-103">SYNAPSE Analytics güvenlik duvarı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab49-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="dab49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dab49-104">SYNTAX</span></span>

### <span data-ttu-id="dab49-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dab49-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dab49-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab49-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dab49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dab49-107">DESCRIPTION</span></span>
<span data-ttu-id="dab49-108">**Update-AzSynapseFirewallRule** cmdlet 'ı bir Azure SYNAPSE Analytics güvenlik duvarı kuralını izler.</span><span class="sxs-lookup"><span data-stu-id="dab49-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="dab49-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dab49-109">EXAMPLES</span></span>

### <span data-ttu-id="dab49-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dab49-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="dab49-111">Bu komut ContosoFirewallRule adındaki güvenlik duvarı kuralını çalışma alanı ContosoFirewallRule adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab49-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="dab49-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dab49-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="dab49-113">Bu komut, ContosoFirewallRule adındaki güvenlik duvarı kuralını ardışık düzen aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dab49-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="dab49-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dab49-114">PARAMETERS</span></span>

### <span data-ttu-id="dab49-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="dab49-115">-AsJob</span></span>
<span data-ttu-id="dab49-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dab49-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dab49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab49-117">-DefaultProfile</span></span>
<span data-ttu-id="dab49-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dab49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dab49-119">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="dab49-119">-EndIpAddress</span></span>
<span data-ttu-id="dab49-120">Güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="dab49-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="dab49-121">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab49-121">Must be IPv4 format.</span></span>
<span data-ttu-id="dab49-122">Startıpaddress 'den büyük veya buna eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab49-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="dab49-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="dab49-123">-Name</span></span>
<span data-ttu-id="dab49-124">Çalışma alanı için firerduvar kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="dab49-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="dab49-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab49-125">-ResourceGroupName</span></span>
<span data-ttu-id="dab49-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dab49-126">Resource group name.</span></span>

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

### <span data-ttu-id="dab49-127">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="dab49-127">-StartIpAddress</span></span>
<span data-ttu-id="dab49-128">Güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="dab49-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="dab49-129">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab49-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dab49-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="dab49-130">-WorkspaceName</span></span>
<span data-ttu-id="dab49-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="dab49-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dab49-132">-</span><span class="sxs-lookup"><span data-stu-id="dab49-132">-WorkspaceObject</span></span>
<span data-ttu-id="dab49-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="dab49-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dab49-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="dab49-134">-Confirm</span></span>
<span data-ttu-id="dab49-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dab49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab49-136">-WhatIf</span></span>
<span data-ttu-id="dab49-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dab49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab49-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dab49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab49-139">CommonParameters</span></span>
<span data-ttu-id="dab49-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dab49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab49-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dab49-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab49-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dab49-142">INPUTS</span></span>

### <span data-ttu-id="dab49-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dab49-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dab49-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dab49-144">OUTPUTS</span></span>

### <span data-ttu-id="dab49-145">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dab49-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="dab49-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dab49-146">NOTES</span></span>

## <span data-ttu-id="dab49-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dab49-147">RELATED LINKS</span></span>
