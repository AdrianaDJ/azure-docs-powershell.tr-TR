---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 0d99ec672d75844eca37cb63d63a2c6d7433d04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760431"
---
# <span data-ttu-id="6bb19-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb19-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6bb19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb19-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb19-103">Uygulama ağ geçidi için otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb19-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="6bb19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bb19-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bb19-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb19-106">**Yeni-AzApplicationGatewayAutoscaleConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidi Için otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb19-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="6bb19-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bb19-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb19-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bb19-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="6bb19-109">İlk komut, en az kapasite 3 ile bir otomatik ölçeklendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb19-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="6bb19-110">İkinci komut otomatik ölçeklendirme yapılandırmasıyla bir uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bb19-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="6bb19-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bb19-111">PARAMETERS</span></span>

### <span data-ttu-id="6bb19-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb19-112">-DefaultProfile</span></span>
<span data-ttu-id="6bb19-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bb19-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb19-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="6bb19-114">-MaxCapacity</span></span>
<span data-ttu-id="6bb19-115">Uygulama ağ geçidi için her zaman [ve ücretlendirilecek] Maksimum Kapasite birimleri.</span><span class="sxs-lookup"><span data-stu-id="6bb19-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb19-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="6bb19-116">-MinCapacity</span></span>
<span data-ttu-id="6bb19-117">Uygulama ağ geçidi için her zaman [ve ücretlendirilen] olan minimum kapasite birimleri.</span><span class="sxs-lookup"><span data-stu-id="6bb19-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="6bb19-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bb19-118">-Confirm</span></span>
<span data-ttu-id="6bb19-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bb19-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb19-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb19-120">-WhatIf</span></span>
<span data-ttu-id="6bb19-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bb19-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb19-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bb19-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb19-123">CommonParameters</span></span>
<span data-ttu-id="6bb19-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bb19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb19-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb19-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb19-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bb19-126">INPUTS</span></span>

### <span data-ttu-id="6bb19-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6bb19-127">None</span></span>

## <span data-ttu-id="6bb19-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bb19-128">OUTPUTS</span></span>

### <span data-ttu-id="6bb19-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb19-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6bb19-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bb19-130">NOTES</span></span>

## <span data-ttu-id="6bb19-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bb19-131">RELATED LINKS</span></span>

[<span data-ttu-id="6bb19-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb19-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6bb19-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb19-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6bb19-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bb19-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)