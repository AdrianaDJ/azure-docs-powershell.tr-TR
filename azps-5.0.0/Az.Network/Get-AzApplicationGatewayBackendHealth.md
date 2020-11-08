---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278359"
---
# <span data-ttu-id="48ae2-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="48ae2-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="48ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="48ae2-103">Uygulama ağ geçidi uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="48ae2-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="48ae2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48ae2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ae2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="48ae2-106">Get-AzApplicationGatewayBackendHealth cmdlet 'i uygulama ağ geçidi uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="48ae2-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="48ae2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="48ae2-108">Örnek 1: genişletilmiş kaynaklar olmadan arka uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="48ae2-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="48ae2-109">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidinin arka uç durumunu alır ve $BackendHealth değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="48ae2-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="48ae2-110">Örnek 2: genişletilmiş kaynaklarla arka uç durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="48ae2-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="48ae2-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki uygulama ağ geçidinin arka uç durumunu (genişletilmiş kaynaklarla birlikte) alır ve $BackendHealth değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="48ae2-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="48ae2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48ae2-112">PARAMETERS</span></span>

### <span data-ttu-id="48ae2-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="48ae2-113">-AsJob</span></span>
<span data-ttu-id="48ae2-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="48ae2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48ae2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ae2-115">-DefaultProfile</span></span>
<span data-ttu-id="48ae2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48ae2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48ae2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="48ae2-117">-ExpandResource</span></span>
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

### <span data-ttu-id="48ae2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="48ae2-118">-Name</span></span>
<span data-ttu-id="48ae2-119">Bu cmdlet 'in aldığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48ae2-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="48ae2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ae2-120">-ResourceGroupName</span></span>
<span data-ttu-id="48ae2-121">Uygulama ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48ae2-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="48ae2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ae2-122">CommonParameters</span></span>
<span data-ttu-id="48ae2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48ae2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ae2-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48ae2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ae2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48ae2-125">INPUTS</span></span>

### <span data-ttu-id="48ae2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="48ae2-126">System.String</span></span>

## <span data-ttu-id="48ae2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48ae2-127">OUTPUTS</span></span>

### <span data-ttu-id="48ae2-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="48ae2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="48ae2-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48ae2-129">NOTES</span></span>
<span data-ttu-id="48ae2-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="48ae2-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="48ae2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48ae2-131">RELATED LINKS</span></span>

[<span data-ttu-id="48ae2-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48ae2-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

