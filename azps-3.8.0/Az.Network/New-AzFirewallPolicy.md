---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937228"
---
# <span data-ttu-id="90473-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="90473-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="90473-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90473-102">SYNOPSIS</span></span>
<span data-ttu-id="90473-103">Yeni bir Azure Güvenlik Duvarı Ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="90473-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="90473-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90473-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90473-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90473-105">DESCRIPTION</span></span>
<span data-ttu-id="90473-106">**New-AzFirewallPolicy** cmdlet 'ı bir Azure Güvenlik duvarı ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90473-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="90473-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90473-107">EXAMPLES</span></span>

### <span data-ttu-id="90473-108">1. boş ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="90473-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="90473-109">Bu örnek bir Azure Güvenlik duvarı ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="90473-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="90473-110">2. Threatıntel moduyla boş bir ilke oluşturma</span><span class="sxs-lookup"><span data-stu-id="90473-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="90473-111">Bu örnek, tehdit Intel modunu içeren bir Azure Güvenlik duvarı ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="90473-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="90473-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90473-112">PARAMETERS</span></span>

### <span data-ttu-id="90473-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="90473-113">-AsJob</span></span>
<span data-ttu-id="90473-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="90473-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90473-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="90473-115">-BasePolicy</span></span>
<span data-ttu-id="90473-116">Tehdit yönetim bilgileri için işlem modu.</span><span class="sxs-lookup"><span data-stu-id="90473-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="90473-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90473-117">-DefaultProfile</span></span>
<span data-ttu-id="90473-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90473-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90473-119">-Force</span><span class="sxs-lookup"><span data-stu-id="90473-119">-Force</span></span>
<span data-ttu-id="90473-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="90473-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="90473-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="90473-121">-Location</span></span>
<span data-ttu-id="90473-122">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="90473-122">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90473-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="90473-123">-Name</span></span>
<span data-ttu-id="90473-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="90473-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90473-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90473-125">-ResourceGroupName</span></span>
<span data-ttu-id="90473-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="90473-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90473-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="90473-127">-Tag</span></span>
<span data-ttu-id="90473-128">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="90473-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="90473-129">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="90473-129">-ThreatIntelMode</span></span>
<span data-ttu-id="90473-130">Tehdit yönetim bilgileri için işlem modu.</span><span class="sxs-lookup"><span data-stu-id="90473-130">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="90473-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="90473-131">-Confirm</span></span>
<span data-ttu-id="90473-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90473-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90473-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90473-133">-WhatIf</span></span>
<span data-ttu-id="90473-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90473-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90473-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90473-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90473-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90473-136">CommonParameters</span></span>
<span data-ttu-id="90473-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90473-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90473-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90473-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90473-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90473-139">INPUTS</span></span>

### <span data-ttu-id="90473-140">System. String</span><span class="sxs-lookup"><span data-stu-id="90473-140">System.String</span></span>

### <span data-ttu-id="90473-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90473-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90473-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90473-142">OUTPUTS</span></span>

### <span data-ttu-id="90473-143">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="90473-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="90473-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90473-144">NOTES</span></span>

## <span data-ttu-id="90473-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90473-145">RELATED LINKS</span></span>
