---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572726"
---
# <span data-ttu-id="ba570-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="ba570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba570-102">SYNOPSIS</span></span>
<span data-ttu-id="ba570-103">Değiştirilmiş Güvenlik duvarını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ba570-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba570-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba570-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba570-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba570-105">DESCRIPTION</span></span>
<span data-ttu-id="ba570-106">**Set-AzureRmFirewall** cmdlet 'ı bir Azure Güvenlik duvarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ba570-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="ba570-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba570-107">EXAMPLES</span></span>

### <span data-ttu-id="ba570-108">1: güvenlik duvarı uygulaması kuralı koleksiyonunun güncelleştirme önceliği</span><span class="sxs-lookup"><span data-stu-id="ba570-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="ba570-109">Bu örnekte, bir Azure Güvenlik duvarının varolan kural koleksiyonunun önceliği güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba570-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="ba570-110">"AzureFirewall" kaynak grubunda Azure Güvenlik duvarının "RG" olarak kabul edil, "RG" adlı bir uygulama kuralı koleksiyonu içeriyor</span><span class="sxs-lookup"><span data-stu-id="ba570-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="ba570-111">Set-AzureRmFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.</span><span class="sxs-lookup"><span data-stu-id="ba570-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="ba570-112">2: Azure Güvenlik Duvarı oluşturma ve uygulama kuralı koleksiyonunu daha sonra ayarlama</span><span class="sxs-lookup"><span data-stu-id="ba570-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="ba570-113">Bu örnekte, uygulama kuralı koleksiyonları olmadan önce bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ba570-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="ba570-114">Ardından uygulama kuralı ve uygulama kuralı koleksiyonu oluşturulur, bulutta gerçek yapılandırma etkilenmeksizin güvenlik duvarı nesnesi bellekte değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba570-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="ba570-115">Değişikliklerin bulutta yansıtılması için Set-AzureRmFirewall çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ba570-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="ba570-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba570-116">PARAMETERS</span></span>

### <span data-ttu-id="ba570-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="ba570-117">-AsJob</span></span>
<span data-ttu-id="ba570-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ba570-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba570-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-119">-AzureFirewall</span></span>
<span data-ttu-id="ba570-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba570-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba570-121">-DefaultProfile</span></span>
<span data-ttu-id="ba570-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba570-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba570-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba570-123">-Confirm</span></span>
<span data-ttu-id="ba570-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba570-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba570-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba570-125">-WhatIf</span></span>
<span data-ttu-id="ba570-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba570-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba570-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba570-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba570-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba570-128">CommonParameters</span></span>
<span data-ttu-id="ba570-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba570-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba570-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba570-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba570-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba570-131">INPUTS</span></span>

### <span data-ttu-id="ba570-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-132">PSAzureFirewall</span></span>
<span data-ttu-id="ba570-133">' AzureFirewall ' parametresi ardışık düzenin ' PSAzureFirewall ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ba570-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="ba570-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba570-134">OUTPUTS</span></span>

### <span data-ttu-id="ba570-135">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ba570-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba570-136">NOTES</span></span>

## <span data-ttu-id="ba570-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba570-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba570-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="ba570-139">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="ba570-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ba570-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
