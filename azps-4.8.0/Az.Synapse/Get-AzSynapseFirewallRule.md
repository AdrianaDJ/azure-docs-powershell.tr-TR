---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107482"
---
# <span data-ttu-id="ecea9-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ecea9-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="ecea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecea9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecea9-103">SYNAPSE Analytics güvenlik duvarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="ecea9-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ecea9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecea9-104">SYNTAX</span></span>

### <span data-ttu-id="ecea9-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ecea9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecea9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecea9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecea9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecea9-107">DESCRIPTION</span></span>
<span data-ttu-id="ecea9-108">**Get-AzSynapseFirewallRule** cmdlet 'ı bir Azure SYNAPSE Analytics güvenlik duvarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="ecea9-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="ecea9-109">Bir kural adı belirtmezseniz, bu cmdlet tüm kuralları alır.</span><span class="sxs-lookup"><span data-stu-id="ecea9-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="ecea9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecea9-110">EXAMPLES</span></span>

### <span data-ttu-id="ecea9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ecea9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ecea9-112">Bu komut, çalışma alanı altındaki tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="ecea9-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="ecea9-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ecea9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="ecea9-114">Bu komut, ad alanı contoso</span><span class="sxs-lookup"><span data-stu-id="ecea9-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="ecea9-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ecea9-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="ecea9-116">Bu komut, ardışık düzen aracılığıyla tüm güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="ecea9-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="ecea9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecea9-117">PARAMETERS</span></span>

### <span data-ttu-id="ecea9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecea9-118">-DefaultProfile</span></span>
<span data-ttu-id="ecea9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecea9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecea9-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ecea9-120">-Name</span></span>
<span data-ttu-id="ecea9-121">Çalışma alanı için firerduvar kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="ecea9-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecea9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecea9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecea9-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ecea9-123">Resource group name.</span></span>

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

### <span data-ttu-id="ecea9-124">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ecea9-124">-WorkspaceName</span></span>
<span data-ttu-id="ecea9-125">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ecea9-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ecea9-126">-</span><span class="sxs-lookup"><span data-stu-id="ecea9-126">-WorkSpaceObject</span></span>
<span data-ttu-id="ecea9-127">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ecea9-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ecea9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecea9-128">CommonParameters</span></span>
<span data-ttu-id="ecea9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecea9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecea9-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ecea9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecea9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecea9-131">INPUTS</span></span>

### <span data-ttu-id="ecea9-132">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ecea9-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ecea9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecea9-133">OUTPUTS</span></span>

### <span data-ttu-id="ecea9-134">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ecea9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="ecea9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecea9-135">NOTES</span></span>

## <span data-ttu-id="ecea9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecea9-136">RELATED LINKS</span></span>
