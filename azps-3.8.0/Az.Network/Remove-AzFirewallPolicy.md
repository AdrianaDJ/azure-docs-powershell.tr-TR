---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104046"
---
# <span data-ttu-id="4f2f4-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f2f4-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="4f2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2f4-103">Azure Güvenlik Duvarı Ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="4f2f4-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="4f2f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f2f4-104">SYNTAX</span></span>

### <span data-ttu-id="4f2f4-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2f4-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f2f4-106">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4f2f4-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f2f4-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2f4-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f2f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f2f4-108">DESCRIPTION</span></span>
<span data-ttu-id="4f2f4-109">**Remove-AzFirewallPolicy** cmdlet 'ı bir Azure Güvenlik Duvarı ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="4f2f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f2f4-110">EXAMPLES</span></span>

### <span data-ttu-id="4f2f4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f2f4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="4f2f4-112">Bu örnekte, "TestRg" resourcegroup</span><span class="sxs-lookup"><span data-stu-id="4f2f4-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="4f2f4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4f2f4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="4f2f4-114">Bu örnekte, kimlik güvenlik ilkesi kimliği tarafından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="4f2f4-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4f2f4-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="4f2f4-116">Bu örnekte $fp</span><span class="sxs-lookup"><span data-stu-id="4f2f4-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="4f2f4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f2f4-117">PARAMETERS</span></span>

### <span data-ttu-id="4f2f4-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="4f2f4-118">-AsJob</span></span>
<span data-ttu-id="4f2f4-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4f2f4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f2f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2f4-120">-DefaultProfile</span></span>
<span data-ttu-id="4f2f4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f2f4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4f2f4-122">-Force</span></span>
<span data-ttu-id="4f2f4-123">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4f2f4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f2f4-124">-InputObject</span></span>
<span data-ttu-id="4f2f4-125">AzureFirewall Ilkesi</span><span class="sxs-lookup"><span data-stu-id="4f2f4-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f2f4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f2f4-126">-Name</span></span>
<span data-ttu-id="4f2f4-127">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f2f4-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f2f4-128">-PassThru</span></span>
<span data-ttu-id="4f2f4-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f2f4-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f2f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f2f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f2f4-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f2f4-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f2f4-133">-ResourceId</span></span>
<span data-ttu-id="4f2f4-134">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f2f4-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f2f4-135">-Confirm</span></span>
<span data-ttu-id="4f2f4-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f2f4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f2f4-137">-WhatIf</span></span>
<span data-ttu-id="4f2f4-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f2f4-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f2f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2f4-140">CommonParameters</span></span>
<span data-ttu-id="4f2f4-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2f4-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f2f4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2f4-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f2f4-143">INPUTS</span></span>

### <span data-ttu-id="4f2f4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4f2f4-144">System.String</span></span>

### <span data-ttu-id="4f2f4-145">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f2f4-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="4f2f4-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f2f4-146">OUTPUTS</span></span>

### <span data-ttu-id="4f2f4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f2f4-147">System.Boolean</span></span>

## <span data-ttu-id="4f2f4-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f2f4-148">NOTES</span></span>

## <span data-ttu-id="4f2f4-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f2f4-149">RELATED LINKS</span></span>
