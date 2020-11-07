---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ff3e4f4a69309d2dfa5655fefac3d1c5a0e933f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938079"
---
# <span data-ttu-id="6d9e4-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6d9e4-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="6d9e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9e4-103">Site bağlantılarının üzerine gelmek için sanal ağ geçidinde ayarlanan VPN IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="6d9e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d9e4-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9e4-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6d9e4-107">**Get-Azvpnclientıpsecparameter** cmdlet 'ı, ağ geçidi adına ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinde ayarlanan VPN IPSec parametreleriniz nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="6d9e4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d9e4-108">EXAMPLES</span></span>

### <span data-ttu-id="6d9e4-109">1: site bağlantılarının üzerine gelmek için sanal ağ geçitindeki VPN IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6d9e4-110">Sanal ağ geçitte "myRG" adlı sanal ağ geçidinde ayarlanan VPN IPSec parametrelerinin nesnesini döndürür</span><span class="sxs-lookup"><span data-stu-id="6d9e4-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6d9e4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d9e4-111">PARAMETERS</span></span>

### <span data-ttu-id="6d9e4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9e4-112">-DefaultProfile</span></span>
<span data-ttu-id="6d9e4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9e4-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d9e4-114">-Name</span></span>
<span data-ttu-id="6d9e4-115">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-115">The resource name.</span></span>

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

### <span data-ttu-id="6d9e4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9e4-116">-ResourceGroupName</span></span>
<span data-ttu-id="6d9e4-117">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-117">The resource group name.</span></span>

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

### <span data-ttu-id="6d9e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9e4-118">CommonParameters</span></span>
<span data-ttu-id="6d9e4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9e4-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6d9e4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9e4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d9e4-121">INPUTS</span></span>

### <span data-ttu-id="6d9e4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6d9e4-122">System.String</span></span>

## <span data-ttu-id="6d9e4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d9e4-123">OUTPUTS</span></span>

### <span data-ttu-id="6d9e4-124">Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters</span><span class="sxs-lookup"><span data-stu-id="6d9e4-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="6d9e4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d9e4-125">NOTES</span></span>

## <span data-ttu-id="6d9e4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d9e4-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d9e4-127">Yeni-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="6d9e4-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6d9e4-128">Remove-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="6d9e4-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6d9e4-129">Set-Azvpnclientıpsecparameter</span><span class="sxs-lookup"><span data-stu-id="6d9e4-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
