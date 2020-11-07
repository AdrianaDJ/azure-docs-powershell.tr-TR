---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 652583ff4425c0403440856a32be3b8107d771ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931806"
---
# <span data-ttu-id="20806-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="20806-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="20806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20806-102">SYNOPSIS</span></span>
<span data-ttu-id="20806-103">Uygulama ağ geçidi güvenlik duvarı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="20806-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="20806-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20806-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20806-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20806-105">DESCRIPTION</span></span>
<span data-ttu-id="20806-106">**Get-AzApplicationGatewayFirewallPolicy** cmdlet 'i uygulama ağ geçidi güvenlik ilkesi alır..</span><span class="sxs-lookup"><span data-stu-id="20806-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="20806-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20806-107">EXAMPLES</span></span>

### <span data-ttu-id="20806-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20806-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="20806-109">Bu komut, FirewallPolicy1 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidi güvenlik ilkesini alır ve $AppGwFirewallPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="20806-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="20806-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20806-110">PARAMETERS</span></span>

### <span data-ttu-id="20806-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20806-111">-DefaultProfile</span></span>
<span data-ttu-id="20806-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20806-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20806-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="20806-113">-Name</span></span>
<span data-ttu-id="20806-114">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="20806-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20806-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20806-115">-ResourceGroupName</span></span>
<span data-ttu-id="20806-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="20806-116">The resource group name.</span></span>

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

### <span data-ttu-id="20806-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20806-117">CommonParameters</span></span>
<span data-ttu-id="20806-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20806-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20806-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="20806-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20806-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20806-120">INPUTS</span></span>

### <span data-ttu-id="20806-121">System. String</span><span class="sxs-lookup"><span data-stu-id="20806-121">System.String</span></span>

## <span data-ttu-id="20806-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20806-122">OUTPUTS</span></span>

### <span data-ttu-id="20806-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="20806-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="20806-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20806-124">NOTES</span></span>

## <span data-ttu-id="20806-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20806-125">RELATED LINKS</span></span>