---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589480"
---
# <span data-ttu-id="f91a1-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f91a1-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="f91a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f91a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f91a1-103">ResourceGroupName ve GatewayName kullanarak VpnGateway kaynağını alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="f91a1-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f91a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f91a1-104">SYNTAX</span></span>

### <span data-ttu-id="f91a1-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f91a1-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f91a1-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91a1-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f91a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f91a1-107">DESCRIPTION</span></span>
<span data-ttu-id="f91a1-108">ResourceGroupName ve GatewayName kullanarak VpnGateway kaynağını alır veya tüm ağ geçitlerini ResourceGroupName veya SubscriptionID tarafından listeler.</span><span class="sxs-lookup"><span data-stu-id="f91a1-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="f91a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f91a1-109">EXAMPLES</span></span>

### <span data-ttu-id="f91a1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f91a1-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="f91a1-111">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda bir kaynak grubu, sanal WAN, sanal ağ, Batı ABD 'deki sanal hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f91a1-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f91a1-112">Sanal hub 'da 2 ölçekli birimlerle daha sonra bir VPN ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f91a1-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="f91a1-113">Ardından, resourceGroupName ve ağ geçidi adını kullanarak VpnGateway 'i alır.</span><span class="sxs-lookup"><span data-stu-id="f91a1-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="f91a1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f91a1-114">PARAMETERS</span></span>

### <span data-ttu-id="f91a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91a1-115">-DefaultProfile</span></span>
<span data-ttu-id="f91a1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f91a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91a1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f91a1-117">-Name</span></span>
<span data-ttu-id="f91a1-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f91a1-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="f91a1-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f91a1-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91a1-121">CommonParameters</span></span>
<span data-ttu-id="f91a1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f91a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91a1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f91a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91a1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f91a1-124">INPUTS</span></span>

### <span data-ttu-id="f91a1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f91a1-125">System.String</span></span>

## <span data-ttu-id="f91a1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f91a1-126">OUTPUTS</span></span>

### <span data-ttu-id="f91a1-127">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f91a1-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="f91a1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f91a1-128">NOTES</span></span>

## <span data-ttu-id="f91a1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f91a1-129">RELATED LINKS</span></span>
