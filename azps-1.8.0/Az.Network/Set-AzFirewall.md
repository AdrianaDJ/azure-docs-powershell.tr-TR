---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760014"
---
# <span data-ttu-id="84d7f-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-101">Set-AzFirewall</span></span>

## <span data-ttu-id="84d7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="84d7f-103">Değiştirilmiş Güvenlik duvarını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="84d7f-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="84d7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84d7f-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d7f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="84d7f-106">**Set-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="84d7f-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="84d7f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84d7f-107">EXAMPLES</span></span>

### <span data-ttu-id="84d7f-108">1: güvenlik duvarı uygulaması kuralı koleksiyonunun güncelleştirme önceliği</span><span class="sxs-lookup"><span data-stu-id="84d7f-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="84d7f-109">Bu örnekte, bir Azure Güvenlik duvarının varolan kural koleksiyonunun önceliği güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="84d7f-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="84d7f-110">"AzureFirewall" kaynak grubunda Azure Güvenlik duvarının "RG" olarak kabul edil, "RG" adlı bir uygulama kuralı koleksiyonu içeriyor</span><span class="sxs-lookup"><span data-stu-id="84d7f-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="84d7f-111">Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="84d7f-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="84d7f-112">2: Azure Güvenlik Duvarı oluşturma ve uygulama kuralı koleksiyonunu daha sonra ayarlama</span><span class="sxs-lookup"><span data-stu-id="84d7f-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="84d7f-113">Bu örnekte, uygulama kuralı koleksiyonları olmadan önce bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84d7f-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="84d7f-114">Ardından uygulama kuralı ve uygulama kuralı koleksiyonu oluşturulur, bulutta gerçek yapılandırma etkilenmeksizin güvenlik duvarı nesnesi bellekte değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="84d7f-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="84d7f-115">Değişikliklerin bulutta yansıtılması için Set-AzFirewall çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84d7f-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="84d7f-116">3: Azure Güvenlik duvarının tehdit Intel işlem modunu güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="84d7f-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="84d7f-117">Bu örnekte, "RG" kaynak grubundaki "AzureFirewall" Azure Güvenlik duvarının tehdit Intel çalışma modu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="84d7f-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="84d7f-118">Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="84d7f-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="84d7f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84d7f-119">PARAMETERS</span></span>

### <span data-ttu-id="84d7f-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="84d7f-120">-AsJob</span></span>
<span data-ttu-id="84d7f-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="84d7f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84d7f-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-122">-AzureFirewall</span></span>
<span data-ttu-id="84d7f-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-123">The AzureFirewall</span></span>

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

### <span data-ttu-id="84d7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d7f-124">-DefaultProfile</span></span>
<span data-ttu-id="84d7f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84d7f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84d7f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="84d7f-126">-Confirm</span></span>
<span data-ttu-id="84d7f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84d7f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d7f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d7f-128">-WhatIf</span></span>
<span data-ttu-id="84d7f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84d7f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84d7f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84d7f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d7f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d7f-131">CommonParameters</span></span>
<span data-ttu-id="84d7f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84d7f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d7f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d7f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d7f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84d7f-134">INPUTS</span></span>

### <span data-ttu-id="84d7f-135">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="84d7f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84d7f-136">OUTPUTS</span></span>

### <span data-ttu-id="84d7f-137">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="84d7f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84d7f-138">NOTES</span></span>

## <span data-ttu-id="84d7f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84d7f-139">RELATED LINKS</span></span>

[<span data-ttu-id="84d7f-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="84d7f-141">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="84d7f-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="84d7f-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
