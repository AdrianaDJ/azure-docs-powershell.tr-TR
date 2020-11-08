---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105489"
---
# <span data-ttu-id="41b83-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="41b83-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="41b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b83-102">SYNOPSIS</span></span>
<span data-ttu-id="41b83-103">Zorunlu tünel trafiğinin varsayılan yolunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="41b83-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="41b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41b83-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41b83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41b83-105">DESCRIPTION</span></span>
<span data-ttu-id="41b83-106">**Remove-AzureVNetGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel trafiği için şirket içi sitesinin varsayılan yolunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="41b83-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="41b83-107">Bu cmdlet, bir sanal ağın Azure sanal özel ağ (VPN) ağ geçidinden yolunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="41b83-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="41b83-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41b83-108">EXAMPLES</span></span>

### <span data-ttu-id="41b83-109">Örnek 1: varsayılan siteye bir yol kaldırma</span><span class="sxs-lookup"><span data-stu-id="41b83-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="41b83-110">Bu komut, ContosoVNet01 adındaki sanal ağın VPN 'sinden varsayılan site yolunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="41b83-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="41b83-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41b83-111">PARAMETERS</span></span>

### <span data-ttu-id="41b83-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="41b83-112">-Profile</span></span>
<span data-ttu-id="41b83-113">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="41b83-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41b83-114">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="41b83-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b83-115">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="41b83-115">-VNetName</span></span>
<span data-ttu-id="41b83-116">Sanal ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="41b83-116">Specifies a virtual network.</span></span>
<span data-ttu-id="41b83-117">Bu cmdlet, bu parametrenin belirttiği sanal ağın VPN ağ geçidinden varsayılan yolunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="41b83-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b83-118">CommonParameters</span></span>
<span data-ttu-id="41b83-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41b83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b83-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b83-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b83-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41b83-121">INPUTS</span></span>

## <span data-ttu-id="41b83-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41b83-122">OUTPUTS</span></span>

## <span data-ttu-id="41b83-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41b83-123">NOTES</span></span>

## <span data-ttu-id="41b83-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41b83-124">RELATED LINKS</span></span>

[<span data-ttu-id="41b83-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="41b83-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
