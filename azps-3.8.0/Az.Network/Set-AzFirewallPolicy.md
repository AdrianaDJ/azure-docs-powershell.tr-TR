---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097988"
---
# <span data-ttu-id="65d5c-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="65d5c-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="65d5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="65d5c-103">Değiştirilmiş bir Azure Güvenlik Duvarı ilkesini kaydeder</span><span class="sxs-lookup"><span data-stu-id="65d5c-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="65d5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65d5c-104">SYNTAX</span></span>

### <span data-ttu-id="65d5c-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65d5c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d5c-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65d5c-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d5c-107">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="65d5c-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65d5c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="65d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="65d5c-109">**Set-AzFirewallPolicy** cmdlet 'ı bir Azure Güvenlik Duvarı ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65d5c-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="65d5c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65d5c-110">EXAMPLES</span></span>

### <span data-ttu-id="65d5c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65d5c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="65d5c-112">Bu örnekte, güvenlik duvarı ilkesi yeni güvenlik duvarı ilke değeriyle ayarlanır</span><span class="sxs-lookup"><span data-stu-id="65d5c-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="65d5c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="65d5c-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="65d5c-114">Bu örnekte, güvenlik duvarı ilkesi yeni tehdit Intel moduyla ayarlanır</span><span class="sxs-lookup"><span data-stu-id="65d5c-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="65d5c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65d5c-115">PARAMETERS</span></span>

### <span data-ttu-id="65d5c-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="65d5c-116">-AsJob</span></span>
<span data-ttu-id="65d5c-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="65d5c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65d5c-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="65d5c-118">-BasePolicy</span></span>
<span data-ttu-id="65d5c-119">Devralınacağı temel ilke</span><span class="sxs-lookup"><span data-stu-id="65d5c-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d5c-120">-DefaultProfile</span></span>
<span data-ttu-id="65d5c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65d5c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d5c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65d5c-122">-InputObject</span></span>
<span data-ttu-id="65d5c-123">AzureFirewall Ilkesi</span><span class="sxs-lookup"><span data-stu-id="65d5c-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="65d5c-124">-Location</span></span>
<span data-ttu-id="65d5c-125">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="65d5c-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="65d5c-126">-Name</span></span>
<span data-ttu-id="65d5c-127">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="65d5c-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d5c-128">-ResourceGroupName</span></span>
<span data-ttu-id="65d5c-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="65d5c-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65d5c-130">-ResourceId</span></span>
<span data-ttu-id="65d5c-131">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="65d5c-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="65d5c-132">-Tag</span></span>
<span data-ttu-id="65d5c-133">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="65d5c-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-134">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="65d5c-134">-ThreatIntelMode</span></span>
<span data-ttu-id="65d5c-135">Tehdit yönetim bilgileri için işlem modu.</span><span class="sxs-lookup"><span data-stu-id="65d5c-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d5c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="65d5c-136">-Confirm</span></span>
<span data-ttu-id="65d5c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65d5c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d5c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d5c-138">-WhatIf</span></span>
<span data-ttu-id="65d5c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65d5c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d5c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65d5c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d5c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d5c-141">CommonParameters</span></span>
<span data-ttu-id="65d5c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65d5c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d5c-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65d5c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d5c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65d5c-144">INPUTS</span></span>

### <span data-ttu-id="65d5c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="65d5c-145">System.String</span></span>

### <span data-ttu-id="65d5c-146">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="65d5c-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="65d5c-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65d5c-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65d5c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65d5c-148">OUTPUTS</span></span>

### <span data-ttu-id="65d5c-149">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="65d5c-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="65d5c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65d5c-150">NOTES</span></span>

## <span data-ttu-id="65d5c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65d5c-151">RELATED LINKS</span></span>
