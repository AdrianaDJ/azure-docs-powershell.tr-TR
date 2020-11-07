---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760060"
---
# <span data-ttu-id="53b23-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53b23-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="53b23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b23-102">SYNOPSIS</span></span>
<span data-ttu-id="53b23-103">Uygulama ağ geçidi güvenlik ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="53b23-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="53b23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53b23-104">SYNTAX</span></span>

### <span data-ttu-id="53b23-105">ByFactoryObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53b23-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b23-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="53b23-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b23-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="53b23-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53b23-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="53b23-108">DESCRIPTION</span></span>
<span data-ttu-id="53b23-109">**Set-AzApplicationGatewayFirewallPolicy** cmdlet 'i, bir Azure uygulama ağ geçidi güvenlik duvarı ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="53b23-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="53b23-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53b23-110">EXAMPLES</span></span>

### <span data-ttu-id="53b23-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53b23-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="53b23-112">Bu komut, uygulama ağ geçidi güvenlik ilkesini $AppGwFirewallPolicy değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGwFirewallPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="53b23-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="53b23-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53b23-113">PARAMETERS</span></span>

### <span data-ttu-id="53b23-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="53b23-114">-AsJob</span></span>
<span data-ttu-id="53b23-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="53b23-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53b23-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="53b23-116">-CustomRule</span></span>
<span data-ttu-id="53b23-117">CustomRules listesi</span><span class="sxs-lookup"><span data-stu-id="53b23-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b23-118">-DefaultProfile</span></span>
<span data-ttu-id="53b23-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53b23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b23-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53b23-120">-InputObject</span></span>
<span data-ttu-id="53b23-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53b23-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53b23-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="53b23-122">-Name</span></span>
<span data-ttu-id="53b23-123">Güvenlik Duvarı Ilke adı.</span><span class="sxs-lookup"><span data-stu-id="53b23-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53b23-124">-ResourceGroupName</span></span>
<span data-ttu-id="53b23-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="53b23-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b23-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53b23-126">-ResourceId</span></span>
<span data-ttu-id="53b23-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="53b23-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b23-128">CommonParameters</span></span>
<span data-ttu-id="53b23-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53b23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b23-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b23-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b23-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53b23-131">INPUTS</span></span>

### <span data-ttu-id="53b23-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53b23-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="53b23-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53b23-133">OUTPUTS</span></span>

### <span data-ttu-id="53b23-134">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53b23-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="53b23-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53b23-135">NOTES</span></span>

## <span data-ttu-id="53b23-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53b23-136">RELATED LINKS</span></span>
