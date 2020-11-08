---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278327"
---
# <span data-ttu-id="d1f23-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d1f23-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="d1f23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f23-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f23-103">Güvenlik duvarı uygulaması kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1f23-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="d1f23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1f23-104">SYNTAX</span></span>

### <span data-ttu-id="d1f23-105">TargetFqdn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1f23-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f23-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d1f23-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1f23-107">DESCRIPTION</span></span>
<span data-ttu-id="d1f23-108">**New-AzFirewallApplicationRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir uygulama kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1f23-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="d1f23-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1f23-109">EXAMPLES</span></span>

### <span data-ttu-id="d1f23-110">Örnek 1:10.0.0.0 'den tüm HTTPS trafiğine izin veren bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1f23-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="d1f23-111">Bu örnek, bağlantı noktası 443 üzerindeki HTTPS trafiğinin 10.0.0.0 'den izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1f23-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="d1f23-112">Örnek 2:10.0.0.0/24 alt ağı için WindowsUpdate için bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1f23-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="d1f23-113">Bu örnek, 10.0.0.0/24 etki alanı için Windows güncelleştirmelerinde trafiğe izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1f23-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="d1f23-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1f23-114">PARAMETERS</span></span>

### <span data-ttu-id="d1f23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f23-115">-DefaultProfile</span></span>
<span data-ttu-id="d1f23-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1f23-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1f23-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d1f23-117">-Description</span></span>
<span data-ttu-id="d1f23-118">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1f23-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d1f23-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d1f23-119">-FqdnTag</span></span>
<span data-ttu-id="d1f23-120">Bu kural için FQDN etiketlerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="d1f23-121">Kullanılabilir Etiketler [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet 'i kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1f23-122">-Name</span></span>
<span data-ttu-id="d1f23-123">Bu uygulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="d1f23-124">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d1f23-124">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d1f23-125">-Protocol</span></span>
<span data-ttu-id="d1f23-126">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="d1f23-127">Biçim <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="d1f23-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="d1f23-128">Örneğin, "http: 80" veya "https: 443".</span><span class="sxs-lookup"><span data-stu-id="d1f23-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="d1f23-129">TargetFqdn kullanıldığında protokol zorunludur, ancak FqdnTag ile kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="d1f23-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="d1f23-130">Desteklenen protokoller HTTP ve HTTPS 'DIR.</span><span class="sxs-lookup"><span data-stu-id="d1f23-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d1f23-131">-SourceAddress</span></span>
<span data-ttu-id="d1f23-132">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="d1f23-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-133">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="d1f23-133">-SourceIpGroup</span></span>
<span data-ttu-id="d1f23-134">Kuralın kaynak ıpgroup 'u</span><span class="sxs-lookup"><span data-stu-id="d1f23-134">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="d1f23-135">-TargetFqdn</span></span>
<span data-ttu-id="d1f23-136">Bu kurala göre filtrelenmiş etki alanı adlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="d1f23-137">Yıldız işareti (' '), *yalnızca listedeki BIR FQDN 'nin ilk karakteri olarak kabul edilir. Kullanıldığında yıldız işareti herhangi bir sayıda karakterle eşleşir. (örneğin, '* msn.com ', msn.com ve tüm alt etki alanlarına eşleşir)</span><span class="sxs-lookup"><span data-stu-id="d1f23-137">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1f23-138">-Confirm</span></span>
<span data-ttu-id="d1f23-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1f23-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f23-140">-WhatIf</span></span>
<span data-ttu-id="d1f23-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1f23-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f23-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1f23-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f23-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f23-143">CommonParameters</span></span>
<span data-ttu-id="d1f23-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1f23-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f23-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f23-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f23-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1f23-146">INPUTS</span></span>

### <span data-ttu-id="d1f23-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d1f23-147">None</span></span>

## <span data-ttu-id="d1f23-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1f23-148">OUTPUTS</span></span>

### <span data-ttu-id="d1f23-149">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d1f23-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="d1f23-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1f23-150">NOTES</span></span>

## <span data-ttu-id="d1f23-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1f23-151">RELATED LINKS</span></span>

[<span data-ttu-id="d1f23-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d1f23-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="d1f23-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d1f23-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d1f23-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d1f23-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d1f23-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d1f23-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
