---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588461"
---
# <span data-ttu-id="afeab-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="afeab-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="afeab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afeab-102">SYNOPSIS</span></span>
<span data-ttu-id="afeab-103">Otomatik ölçeklendirme yapılandırmasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="afeab-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afeab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afeab-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afeab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afeab-105">DESCRIPTION</span></span>
<span data-ttu-id="afeab-106">**Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet 'i var olan uygulama ağ geçidinden otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="afeab-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="afeab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afeab-107">EXAMPLES</span></span>

### <span data-ttu-id="afeab-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="afeab-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="afeab-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="afeab-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="afeab-110">İkinci komut, applicationg ağ geçidinden otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="afeab-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="afeab-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="afeab-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="afeab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afeab-112">PARAMETERS</span></span>

### <span data-ttu-id="afeab-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afeab-113">-ApplicationGateway</span></span>
<span data-ttu-id="afeab-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afeab-114">The applicationGateway</span></span>

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

### <span data-ttu-id="afeab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afeab-115">-DefaultProfile</span></span>
<span data-ttu-id="afeab-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afeab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afeab-117">-Force</span><span class="sxs-lookup"><span data-stu-id="afeab-117">-Force</span></span>
<span data-ttu-id="afeab-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="afeab-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="afeab-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="afeab-119">-Confirm</span></span>
<span data-ttu-id="afeab-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afeab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afeab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afeab-121">-WhatIf</span></span>
<span data-ttu-id="afeab-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afeab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afeab-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afeab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afeab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afeab-124">CommonParameters</span></span>
<span data-ttu-id="afeab-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afeab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afeab-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afeab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afeab-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afeab-127">INPUTS</span></span>

### <span data-ttu-id="afeab-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afeab-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="afeab-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afeab-129">OUTPUTS</span></span>

### <span data-ttu-id="afeab-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afeab-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="afeab-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afeab-131">NOTES</span></span>

## <span data-ttu-id="afeab-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afeab-132">RELATED LINKS</span></span>
