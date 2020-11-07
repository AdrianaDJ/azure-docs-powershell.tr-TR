---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937217"
---
# <span data-ttu-id="b0447-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b0447-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="b0447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0447-102">SYNOPSIS</span></span>
<span data-ttu-id="b0447-103">Yeni Azure Güvenlik Duvarı Ilkesi uygulama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0447-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="b0447-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0447-104">SYNTAX</span></span>

### <span data-ttu-id="b0447-105">TargetFqdn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0447-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0447-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="b0447-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0447-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0447-107">DESCRIPTION</span></span>
<span data-ttu-id="b0447-108">**New-AzFirewallPolicyApplicationRule** cmdlet 'ı, Azure Güvenlik duvarı ilkesi Için bir uygulama kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0447-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="b0447-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0447-109">EXAMPLES</span></span>

### <span data-ttu-id="b0447-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b0447-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="b0447-111">Bu örnek, kaynak adresi, protokol ve hedef FQDN 'ler içeren bir uygulama kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0447-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="b0447-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0447-112">PARAMETERS</span></span>

### <span data-ttu-id="b0447-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0447-113">-DefaultProfile</span></span>
<span data-ttu-id="b0447-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0447-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0447-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b0447-115">-Description</span></span>
<span data-ttu-id="b0447-116">Kuralın açıklaması</span><span class="sxs-lookup"><span data-stu-id="b0447-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="b0447-117">-FqdnTag</span></span>
<span data-ttu-id="b0447-118">Kuralın FQDN etiketleri</span><span class="sxs-lookup"><span data-stu-id="b0447-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0447-119">-Name</span></span>
<span data-ttu-id="b0447-120">Uygulama kuralının adı</span><span class="sxs-lookup"><span data-stu-id="b0447-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-121">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b0447-121">-Protocol</span></span>
<span data-ttu-id="b0447-122">Kuralın protokolleri</span><span class="sxs-lookup"><span data-stu-id="b0447-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b0447-123">-SourceAddress</span></span>
<span data-ttu-id="b0447-124">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="b0447-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="b0447-125">-TargetFqdn</span></span>
<span data-ttu-id="b0447-126">Kuralın hedef FQDN 'leri</span><span class="sxs-lookup"><span data-stu-id="b0447-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0447-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0447-127">-Confirm</span></span>
<span data-ttu-id="b0447-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0447-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0447-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0447-129">-WhatIf</span></span>
<span data-ttu-id="b0447-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0447-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0447-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0447-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0447-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0447-132">CommonParameters</span></span>
<span data-ttu-id="b0447-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0447-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0447-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b0447-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0447-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0447-135">INPUTS</span></span>

### <span data-ttu-id="b0447-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b0447-136">None</span></span>

## <span data-ttu-id="b0447-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0447-137">OUTPUTS</span></span>

### <span data-ttu-id="b0447-138">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b0447-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="b0447-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0447-139">NOTES</span></span>

## <span data-ttu-id="b0447-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0447-140">RELATED LINKS</span></span>
