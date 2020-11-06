---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591939"
---
# <span data-ttu-id="e90ee-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e90ee-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="e90ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e90ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e90ee-103">Uygulama ağ geçidinin otomatik ölçeklendirme yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e90ee-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e90ee-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e90ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e90ee-105">DESCRIPTION</span></span>
<span data-ttu-id="e90ee-106">**Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet 'ı, uygulama ağ geçidinin varolan otomatik ölçeklendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e90ee-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="e90ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e90ee-107">EXAMPLES</span></span>

### <span data-ttu-id="e90ee-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e90ee-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e90ee-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e90ee-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="e90ee-110">İkinci komut, applicationg ağ geçidinden otomatik ölçeklendirme yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e90ee-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="e90ee-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e90ee-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e90ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e90ee-112">PARAMETERS</span></span>

### <span data-ttu-id="e90ee-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e90ee-113">-ApplicationGateway</span></span>
<span data-ttu-id="e90ee-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e90ee-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e90ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90ee-115">-DefaultProfile</span></span>
<span data-ttu-id="e90ee-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e90ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e90ee-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="e90ee-117">-MinCapacity</span></span>
<span data-ttu-id="e90ee-118">Uygulama ağ geçidi için minimum capcity.</span><span class="sxs-lookup"><span data-stu-id="e90ee-118">Minimum capcity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90ee-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e90ee-119">-Confirm</span></span>
<span data-ttu-id="e90ee-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e90ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e90ee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90ee-121">-WhatIf</span></span>
<span data-ttu-id="e90ee-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e90ee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90ee-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e90ee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e90ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90ee-124">CommonParameters</span></span>
<span data-ttu-id="e90ee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e90ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90ee-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90ee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e90ee-127">INPUTS</span></span>

### <span data-ttu-id="e90ee-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e90ee-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e90ee-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e90ee-129">OUTPUTS</span></span>

### <span data-ttu-id="e90ee-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e90ee-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e90ee-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e90ee-131">NOTES</span></span>

## <span data-ttu-id="e90ee-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e90ee-132">RELATED LINKS</span></span>
