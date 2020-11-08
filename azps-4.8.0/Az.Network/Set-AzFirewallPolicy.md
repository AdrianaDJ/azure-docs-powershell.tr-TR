---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274778"
---
# <span data-ttu-id="3d820-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3d820-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="3d820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d820-102">SYNOPSIS</span></span>
<span data-ttu-id="3d820-103">Değiştirilmiş bir Azure Güvenlik Duvarı ilkesini kaydeder</span><span class="sxs-lookup"><span data-stu-id="3d820-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="3d820-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d820-104">SYNTAX</span></span>

### <span data-ttu-id="3d820-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d820-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d820-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d820-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d820-107">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3d820-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d820-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d820-108">DESCRIPTION</span></span>
<span data-ttu-id="3d820-109">**Set-AzFirewallPolicy** cmdlet 'ı bir Azure Güvenlik Duvarı ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3d820-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="3d820-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d820-110">EXAMPLES</span></span>

### <span data-ttu-id="3d820-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d820-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="3d820-112">Bu örnekte, güvenlik duvarı ilkesi yeni güvenlik duvarı ilke değeriyle ayarlanır</span><span class="sxs-lookup"><span data-stu-id="3d820-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="3d820-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d820-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="3d820-114">Bu örnekte, güvenlik duvarı ilkesi yeni tehdit Intel moduyla ayarlanır</span><span class="sxs-lookup"><span data-stu-id="3d820-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="3d820-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3d820-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="3d820-116">Bu örnekte, güvenlik duvarı ilkesi yeni tehdit Intel Whitelist ile ayarlanır</span><span class="sxs-lookup"><span data-stu-id="3d820-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="3d820-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d820-117">PARAMETERS</span></span>

### <span data-ttu-id="3d820-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d820-118">-AsJob</span></span>
<span data-ttu-id="3d820-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3d820-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="3d820-120">-BasePolicy</span></span>
<span data-ttu-id="3d820-121">Devralınacağı temel ilke</span><span class="sxs-lookup"><span data-stu-id="3d820-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d820-122">-DefaultProfile</span></span>
<span data-ttu-id="3d820-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d820-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="3d820-124">-DnsSetting</span></span>
<span data-ttu-id="3d820-125">DNS ayarı</span><span class="sxs-lookup"><span data-stu-id="3d820-125">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d820-126">-InputObject</span></span>
<span data-ttu-id="3d820-127">AzureFirewall Ilkesi</span><span class="sxs-lookup"><span data-stu-id="3d820-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="3d820-128">-Location</span></span>
<span data-ttu-id="3d820-129">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="3d820-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d820-130">-Name</span></span>
<span data-ttu-id="3d820-131">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3d820-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d820-132">-ResourceGroupName</span></span>
<span data-ttu-id="3d820-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3d820-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d820-134">-ResourceId</span></span>
<span data-ttu-id="3d820-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3d820-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3d820-136">-Tag</span></span>
<span data-ttu-id="3d820-137">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="3d820-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-138">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="3d820-138">-ThreatIntelMode</span></span>
<span data-ttu-id="3d820-139">Tehdit yönetim bilgileri için işlem modu.</span><span class="sxs-lookup"><span data-stu-id="3d820-139">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-140">-Threatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="3d820-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="3d820-141">Tehdit yönetim bilgileri için beyaz liste</span><span class="sxs-lookup"><span data-stu-id="3d820-141">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d820-142">-Confirm</span></span>
<span data-ttu-id="3d820-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d820-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d820-144">-WhatIf</span></span>
<span data-ttu-id="3d820-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d820-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d820-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d820-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d820-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d820-147">CommonParameters</span></span>
<span data-ttu-id="3d820-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d820-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d820-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d820-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d820-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d820-150">INPUTS</span></span>

### <span data-ttu-id="3d820-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3d820-151">System.String</span></span>

### <span data-ttu-id="3d820-152">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3d820-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="3d820-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d820-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d820-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d820-154">OUTPUTS</span></span>

### <span data-ttu-id="3d820-155">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3d820-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3d820-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d820-156">NOTES</span></span>

## <span data-ttu-id="3d820-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d820-157">RELATED LINKS</span></span>
