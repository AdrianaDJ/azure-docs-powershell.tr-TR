---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589491"
---
# <span data-ttu-id="c62cd-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c62cd-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="c62cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c62cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c62cd-103">Site bağlantılarının üzerine gelmek için sanal ağ geçidinde ayarlanan VPN IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c62cd-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c62cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c62cd-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c62cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c62cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c62cd-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="c62cd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c62cd-107">**Get-Azurermvpnclientıpsecparameter** cmdlet 'ı, ağ geçidi adına ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinde ayarlanan VPN IPSec parametrelerinizi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c62cd-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="c62cd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c62cd-108">EXAMPLES</span></span>

### <span data-ttu-id="c62cd-109">1: site bağlantılarının üzerine gelmek için sanal ağ geçitindeki VPN IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c62cd-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c62cd-110">Sanal ağ geçitte "myRG" adlı sanal ağ geçidinde ayarlanan VPN IPSec parametrelerinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="c62cd-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="c62cd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c62cd-111">PARAMETERS</span></span>

### <span data-ttu-id="c62cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62cd-112">-DefaultProfile</span></span>
<span data-ttu-id="c62cd-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c62cd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c62cd-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c62cd-114">-Name</span></span>
<span data-ttu-id="c62cd-115">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c62cd-115">The resource name.</span></span>

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

### <span data-ttu-id="c62cd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62cd-116">-ResourceGroupName</span></span>
<span data-ttu-id="c62cd-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c62cd-117">The resource group name.</span></span>

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

### <span data-ttu-id="c62cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62cd-118">CommonParameters</span></span>
<span data-ttu-id="c62cd-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c62cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62cd-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c62cd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62cd-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c62cd-121">INPUTS</span></span>

### <span data-ttu-id="c62cd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c62cd-122">System.String</span></span>

## <span data-ttu-id="c62cd-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c62cd-123">OUTPUTS</span></span>

### <span data-ttu-id="c62cd-124">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="c62cd-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="c62cd-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c62cd-125">NOTES</span></span>

## <span data-ttu-id="c62cd-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c62cd-126">RELATED LINKS</span></span>
