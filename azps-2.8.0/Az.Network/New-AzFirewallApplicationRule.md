---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: cc3ef8146d7a8ba9f5deb9ad65cf6fcc2dd6ac5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918287"
---
# <span data-ttu-id="dd2e6-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="dd2e6-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="dd2e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2e6-103">Güvenlik duvarı uygulaması kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="dd2e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd2e6-104">SYNTAX</span></span>

### <span data-ttu-id="dd2e6-105">TargetFqdn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd2e6-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2e6-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="dd2e6-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd2e6-107">DESCRIPTION</span></span>
<span data-ttu-id="dd2e6-108">**New-AzFirewallApplicationRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir uygulama kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="dd2e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd2e6-109">EXAMPLES</span></span>

### <span data-ttu-id="dd2e6-110">1:10.0.0.0 'tan tüm HTTPS trafiğine izin veren bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd2e6-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="dd2e6-111">Bu örnek, bağlantı noktası 443 üzerindeki HTTPS trafiğinin 10.0.0.0 'den izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="dd2e6-112">2:10.0.0.0/24 alt ağı için WindowsUpdate 'e izin veren bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd2e6-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="dd2e6-113">Bu örnek, 10.0.0.0/24 etki alanı için Windows güncelleştirmelerinde trafiğe izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="dd2e6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd2e6-114">PARAMETERS</span></span>

### <span data-ttu-id="dd2e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2e6-115">-DefaultProfile</span></span>
<span data-ttu-id="dd2e6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd2e6-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="dd2e6-117">-Description</span></span>
<span data-ttu-id="dd2e6-118">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="dd2e6-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="dd2e6-119">-FqdnTag</span></span>
<span data-ttu-id="dd2e6-120">Bu kural için FQDN etiketlerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="dd2e6-121">Kullanılabilir Etiketler [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet 'i kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="dd2e6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd2e6-122">-Name</span></span>
<span data-ttu-id="dd2e6-123">Bu uygulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="dd2e6-124">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="dd2e6-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="dd2e6-125">-Protocol</span></span>
<span data-ttu-id="dd2e6-126">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="dd2e6-127">Biçim <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="dd2e6-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="dd2e6-128">Örneğin, "http: 80" veya "https: 443".</span><span class="sxs-lookup"><span data-stu-id="dd2e6-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="dd2e6-129">TargetFqdn kullanıldığında protokol zorunludur, ancak FqdnTag ile kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="dd2e6-130">Desteklenen protokoller HTTP ve HTTPS 'DIR.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="dd2e6-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="dd2e6-131">-SourceAddress</span></span>
<span data-ttu-id="dd2e6-132">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="dd2e6-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="dd2e6-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="dd2e6-133">-TargetFqdn</span></span>
<span data-ttu-id="dd2e6-134">Bu kurala göre filtrelenmiş etki alanı adlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="dd2e6-135">Yıldız işareti (' '), *yalnızca listedeki BIR FQDN 'nin ilk karakteri olarak kabul edilir. Kullanıldığında yıldız işareti herhangi bir sayıda karakterle eşleşir. (örneğin, '* msn.com ', msn.com ve tüm alt etki alanlarına eşleşir)</span><span class="sxs-lookup"><span data-stu-id="dd2e6-135">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="dd2e6-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd2e6-136">-Confirm</span></span>
<span data-ttu-id="dd2e6-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2e6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2e6-138">-WhatIf</span></span>
<span data-ttu-id="dd2e6-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2e6-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2e6-141">CommonParameters</span></span>
<span data-ttu-id="dd2e6-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd2e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2e6-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2e6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2e6-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd2e6-144">INPUTS</span></span>

### <span data-ttu-id="dd2e6-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dd2e6-145">None</span></span>

## <span data-ttu-id="dd2e6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd2e6-146">OUTPUTS</span></span>

### <span data-ttu-id="dd2e6-147">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="dd2e6-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="dd2e6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd2e6-148">NOTES</span></span>

## <span data-ttu-id="dd2e6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd2e6-149">RELATED LINKS</span></span>

[<span data-ttu-id="dd2e6-150">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="dd2e6-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="dd2e6-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2e6-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dd2e6-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dd2e6-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dd2e6-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="dd2e6-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
