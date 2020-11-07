---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593209"
---
# <span data-ttu-id="31dfb-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31dfb-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="31dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="31dfb-103">Uygulama ağ geçidi için otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31dfb-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31dfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31dfb-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31dfb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="31dfb-106">**New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet 'ı bir Azure Application Gateway Için otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31dfb-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="31dfb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="31dfb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31dfb-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="31dfb-109">İlk komut, en az kapasite 3 ile bir otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31dfb-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="31dfb-110">İkinci komut otomatik ölçeklendirme yapılandırmasıyla bir uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31dfb-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="31dfb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31dfb-111">PARAMETERS</span></span>

### <span data-ttu-id="31dfb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dfb-112">-DefaultProfile</span></span>
<span data-ttu-id="31dfb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31dfb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31dfb-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="31dfb-114">-MinCapacity</span></span>
<span data-ttu-id="31dfb-115">Uygulama ağ geçidi için her zaman [ve ücretlendirilen] olan minimum kapasite birimleri.</span><span class="sxs-lookup"><span data-stu-id="31dfb-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="31dfb-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="31dfb-116">-Confirm</span></span>
<span data-ttu-id="31dfb-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31dfb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31dfb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31dfb-118">-WhatIf</span></span>
<span data-ttu-id="31dfb-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31dfb-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31dfb-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31dfb-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31dfb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dfb-121">CommonParameters</span></span>
<span data-ttu-id="31dfb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31dfb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dfb-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31dfb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dfb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31dfb-124">INPUTS</span></span>

### <span data-ttu-id="31dfb-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31dfb-125">None</span></span>

## <span data-ttu-id="31dfb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31dfb-126">OUTPUTS</span></span>

### <span data-ttu-id="31dfb-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31dfb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="31dfb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31dfb-128">NOTES</span></span>

## <span data-ttu-id="31dfb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31dfb-129">RELATED LINKS</span></span>