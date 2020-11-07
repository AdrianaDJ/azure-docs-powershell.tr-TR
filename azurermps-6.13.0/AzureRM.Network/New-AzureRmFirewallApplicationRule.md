---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764616"
---
# <span data-ttu-id="34cd3-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="34cd3-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="34cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="34cd3-103">Güvenlik duvarı uygulaması kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34cd3-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34cd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34cd3-104">SYNTAX</span></span>

### <span data-ttu-id="34cd3-105">TargetFqdn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34cd3-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34cd3-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="34cd3-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34cd3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="34cd3-108">**New-AzureRmFirewallApplicationRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir uygulama kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34cd3-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="34cd3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="34cd3-110">1:10.0.0.0 'tan tüm HTTPS trafiğine izin veren bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="34cd3-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="34cd3-111">Bu örnek, bağlantı noktası 443 üzerindeki HTTPS trafiğinin 10.0.0.0 'den izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34cd3-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="34cd3-112">2:10.0.0.0/24 alt ağı için WindowsUpdate 'e izin veren bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="34cd3-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="34cd3-113">Bu örnek, 10.0.0.0/24 etki alanı için Windows güncelleştirmelerinde trafiğe izin verecek bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34cd3-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="34cd3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34cd3-114">PARAMETERS</span></span>

### <span data-ttu-id="34cd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34cd3-115">-DefaultProfile</span></span>
<span data-ttu-id="34cd3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34cd3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cd3-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="34cd3-117">-Description</span></span>
<span data-ttu-id="34cd3-118">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="34cd3-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="34cd3-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="34cd3-119">-FqdnTag</span></span>
<span data-ttu-id="34cd3-120">Bu kural için FQDN etiketlerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="34cd3-121">Kullanılabilir Etiketler [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet 'i kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cd3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="34cd3-122">-Name</span></span>
<span data-ttu-id="34cd3-123">Bu uygulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="34cd3-124">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34cd3-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="34cd3-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="34cd3-125">-Protocol</span></span>
<span data-ttu-id="34cd3-126">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="34cd3-127">Biçim <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="34cd3-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="34cd3-128">Örneğin, "http: 80" veya "https: 443".</span><span class="sxs-lookup"><span data-stu-id="34cd3-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="34cd3-129">TargetFqdn kullanıldığında protokol zorunludur, ancak FqdnTag ile kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="34cd3-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="34cd3-130">Desteklenen protokoller HTTP ve HTTPS 'DIR.</span><span class="sxs-lookup"><span data-stu-id="34cd3-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cd3-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="34cd3-131">-SourceAddress</span></span>
<span data-ttu-id="34cd3-132">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="34cd3-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cd3-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="34cd3-133">-TargetFqdn</span></span>
<span data-ttu-id="34cd3-134">Bu kurala göre filtrelenmiş etki alanı adlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="34cd3-135">' ' Yıldız karakteri, *yalnızca listedeki BIR FQDN 'nin ilk karakteri olarak kabul edilir. Kullanıldığında, yıldız karakteri herhangi bir sayıda karakterle eşleşir. (örneğin, '* msn.com ', msn.com ve tüm alt etki alanlarına eşleşir)</span><span class="sxs-lookup"><span data-stu-id="34cd3-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34cd3-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="34cd3-136">-Confirm</span></span>
<span data-ttu-id="34cd3-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34cd3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34cd3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34cd3-138">-WhatIf</span></span>
<span data-ttu-id="34cd3-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34cd3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34cd3-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34cd3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34cd3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cd3-141">CommonParameters</span></span>
<span data-ttu-id="34cd3-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34cd3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cd3-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34cd3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cd3-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34cd3-144">INPUTS</span></span>

### <span data-ttu-id="34cd3-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34cd3-145">None</span></span>
<span data-ttu-id="34cd3-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="34cd3-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34cd3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34cd3-147">OUTPUTS</span></span>

### <span data-ttu-id="34cd3-148">Microsoft. Azure. Commands. Network. model. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="34cd3-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="34cd3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34cd3-149">NOTES</span></span>

## <span data-ttu-id="34cd3-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34cd3-150">RELATED LINKS</span></span>

[<span data-ttu-id="34cd3-151">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="34cd3-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="34cd3-152">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="34cd3-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="34cd3-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="34cd3-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="34cd3-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="34cd3-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)