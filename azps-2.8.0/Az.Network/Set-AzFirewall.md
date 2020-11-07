---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 6d0935b0b2c5296a5d45d25c56cd7feb9e269a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917912"
---
# <span data-ttu-id="3313e-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-101">Set-AzFirewall</span></span>

## <span data-ttu-id="3313e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3313e-102">SYNOPSIS</span></span>
<span data-ttu-id="3313e-103">Değiştirilmiş Güvenlik duvarını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3313e-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="3313e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3313e-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3313e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3313e-105">DESCRIPTION</span></span>
<span data-ttu-id="3313e-106">**Set-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3313e-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="3313e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3313e-107">EXAMPLES</span></span>

### <span data-ttu-id="3313e-108">1: güvenlik duvarı uygulaması kuralı koleksiyonunun güncelleştirme önceliği</span><span class="sxs-lookup"><span data-stu-id="3313e-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="3313e-109">Bu örnekte, bir Azure Güvenlik duvarının varolan kural koleksiyonunun önceliği güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3313e-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="3313e-110">"AzureFirewall" kaynak grubunda Azure Güvenlik duvarının "RG" olarak kabul edil, "RG" adlı bir uygulama kuralı koleksiyonu içeriyor</span><span class="sxs-lookup"><span data-stu-id="3313e-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="3313e-111">Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="3313e-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="3313e-112">2: Azure Güvenlik Duvarı oluşturma ve uygulama kuralı koleksiyonunu daha sonra ayarlama</span><span class="sxs-lookup"><span data-stu-id="3313e-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="3313e-113">Bu örnekte, uygulama kuralı koleksiyonları olmadan önce bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3313e-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="3313e-114">Ardından uygulama kuralı ve uygulama kuralı koleksiyonu oluşturulur, bulutta gerçek yapılandırma etkilenmeksizin güvenlik duvarı nesnesi bellekte değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="3313e-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="3313e-115">Değişikliklerin bulutta yansıtılması için Set-AzFirewall çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="3313e-116">3: Azure Güvenlik duvarının tehdit Intel işlem modunu güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="3313e-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="3313e-117">Bu örnekte, "RG" kaynak grubundaki "AzureFirewall" Azure Güvenlik duvarının tehdit Intel çalışma modu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3313e-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="3313e-118">Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="3313e-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="3313e-119">4: güvenlik duvarını ayırma ve tahsis etme</span><span class="sxs-lookup"><span data-stu-id="3313e-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```

<span data-ttu-id="3313e-120">Bu örnek bir güvenlik duvarı alır, güvenlik duvarını ayırır ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3313e-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="3313e-121">Serbest bırakma komutu, çalışan hizmeti kaldırır ancak güvenlik duvarının yapılandırmasını korur.</span><span class="sxs-lookup"><span data-stu-id="3313e-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="3313e-122">Değişikliklerin bulutta yansıtılması için Set-AzFirewall çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="3313e-123">Kullanıcı Hizmeti yeniden başlatmak istiyorsa, ayırma yöntemi güvenlik duvarında çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="3313e-124">Yeni VNet ve genel IP, güvenlik duvarıyla aynı kaynak grubunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="3313e-125">Değişikliklerin bulutta yansıtılması için, Set-AzFirewall çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="3313e-126">5: Azure Güvenlik duvarına ortak IP adresi ekleme</span><span class="sxs-lookup"><span data-stu-id="3313e-126">5:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="3313e-127">Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3313e-127">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="3313e-128">6: Azure güvenlik duvarından genel IP adresini kaldırma</span><span class="sxs-lookup"><span data-stu-id="3313e-128">6:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="3313e-129">Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarından ayrılır.</span><span class="sxs-lookup"><span data-stu-id="3313e-129">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

## <span data-ttu-id="3313e-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3313e-130">PARAMETERS</span></span>

### <span data-ttu-id="3313e-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="3313e-131">-AsJob</span></span>
<span data-ttu-id="3313e-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3313e-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3313e-133">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-133">-AzureFirewall</span></span>
<span data-ttu-id="3313e-134">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-134">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3313e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3313e-135">-DefaultProfile</span></span>
<span data-ttu-id="3313e-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3313e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3313e-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="3313e-137">-Confirm</span></span>
<span data-ttu-id="3313e-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3313e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3313e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3313e-139">-WhatIf</span></span>
<span data-ttu-id="3313e-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3313e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3313e-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3313e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3313e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3313e-142">CommonParameters</span></span>
<span data-ttu-id="3313e-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3313e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3313e-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3313e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3313e-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3313e-145">INPUTS</span></span>

### <span data-ttu-id="3313e-146">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3313e-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3313e-147">OUTPUTS</span></span>

### <span data-ttu-id="3313e-148">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3313e-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3313e-149">NOTES</span></span>

## <span data-ttu-id="3313e-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3313e-150">RELATED LINKS</span></span>

[<span data-ttu-id="3313e-151">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-151">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="3313e-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="3313e-153">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3313e-153">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
