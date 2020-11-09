---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323809"
---
# <span data-ttu-id="11fef-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="11fef-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="11fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11fef-102">SYNOPSIS</span></span>
<span data-ttu-id="11fef-103">Yeni bir Azure Güvenlik Duvarı Ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="11fef-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="11fef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11fef-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11fef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11fef-105">DESCRIPTION</span></span>
<span data-ttu-id="11fef-106">**New-AzFirewallPolicy** cmdlet 'ı bir Azure Güvenlik duvarı ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11fef-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="11fef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11fef-107">EXAMPLES</span></span>

### <span data-ttu-id="11fef-108">Örnek 1:1.</span><span class="sxs-lookup"><span data-stu-id="11fef-108">Example 1: 1.</span></span> <span data-ttu-id="11fef-109">Boş ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="11fef-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="11fef-110">Bu örnek bir Azure Güvenlik duvarı ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="11fef-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="11fef-111">Örnek 2:2.</span><span class="sxs-lookup"><span data-stu-id="11fef-111">Example 2: 2.</span></span> <span data-ttu-id="11fef-112">Threatıntel moduyla boş bir ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="11fef-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="11fef-113">Bu örnek, tehdit Intel modunu içeren bir Azure Güvenlik duvarı ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="11fef-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="11fef-114">Örnek 3:3.</span><span class="sxs-lookup"><span data-stu-id="11fef-114">Example 3: 3.</span></span> <span data-ttu-id="11fef-115">Threatıntel Whitelist ile boş bir ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="11fef-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="11fef-116">Bu örnek, tehdit Intel Whitelist ile Azure Güvenlik duvarı ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="11fef-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="11fef-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11fef-117">PARAMETERS</span></span>

### <span data-ttu-id="11fef-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="11fef-118">-AsJob</span></span>
<span data-ttu-id="11fef-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="11fef-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11fef-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="11fef-120">-BasePolicy</span></span>
<span data-ttu-id="11fef-121">Devralınacağı temel ilke</span><span class="sxs-lookup"><span data-stu-id="11fef-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="11fef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fef-122">-DefaultProfile</span></span>
<span data-ttu-id="11fef-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11fef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11fef-124">-Force</span><span class="sxs-lookup"><span data-stu-id="11fef-124">-Force</span></span>
<span data-ttu-id="11fef-125">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="11fef-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="11fef-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="11fef-126">-Location</span></span>
<span data-ttu-id="11fef-127">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="11fef-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fef-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="11fef-128">-Name</span></span>
<span data-ttu-id="11fef-129">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="11fef-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fef-130">-ResourceGroupName</span></span>
<span data-ttu-id="11fef-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="11fef-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fef-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="11fef-132">-Tag</span></span>
<span data-ttu-id="11fef-133">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="11fef-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="11fef-134">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="11fef-134">-ThreatIntelMode</span></span>
<span data-ttu-id="11fef-135">Tehdit yönetim bilgileri için işlem modu.</span><span class="sxs-lookup"><span data-stu-id="11fef-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="11fef-136">-Threatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="11fef-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="11fef-137">Tehdit yönetim bilgileri için beyaz liste</span><span class="sxs-lookup"><span data-stu-id="11fef-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="11fef-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="11fef-138">-DnsSetting</span></span>
<span data-ttu-id="11fef-139">DNS ayarı</span><span class="sxs-lookup"><span data-stu-id="11fef-139">The DNS Setting</span></span>

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

### <span data-ttu-id="11fef-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="11fef-140">-Confirm</span></span>
<span data-ttu-id="11fef-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11fef-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11fef-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11fef-142">-WhatIf</span></span>
<span data-ttu-id="11fef-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11fef-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11fef-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11fef-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11fef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fef-145">CommonParameters</span></span>
<span data-ttu-id="11fef-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11fef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fef-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="11fef-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fef-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11fef-148">INPUTS</span></span>

### <span data-ttu-id="11fef-149">System. String</span><span class="sxs-lookup"><span data-stu-id="11fef-149">System.String</span></span>

### <span data-ttu-id="11fef-150">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11fef-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11fef-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11fef-151">OUTPUTS</span></span>

### <span data-ttu-id="11fef-152">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="11fef-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="11fef-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11fef-153">NOTES</span></span>

## <span data-ttu-id="11fef-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11fef-154">RELATED LINKS</span></span>
