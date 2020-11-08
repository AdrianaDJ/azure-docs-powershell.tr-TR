---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106413"
---
# <span data-ttu-id="fd218-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fd218-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="fd218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd218-102">SYNOPSIS</span></span>
<span data-ttu-id="fd218-103">Zorunlu tünel trafiği için varsayılan siteyi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fd218-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="fd218-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd218-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd218-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd218-105">DESCRIPTION</span></span>
<span data-ttu-id="fd218-106">**Set-AzureVNetGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel trafiği için şirket içi sitesine varsayılan yol ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fd218-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="fd218-107">Bu komut, bir sanal ağın Azure sanal özel ağ (VPN) ağ geçidinde yolunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fd218-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="fd218-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd218-108">EXAMPLES</span></span>

## <span data-ttu-id="fd218-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd218-109">PARAMETERS</span></span>

### <span data-ttu-id="fd218-110">-Defaultsıte</span><span class="sxs-lookup"><span data-stu-id="fd218-110">-DefaultSite</span></span>
<span data-ttu-id="fd218-111">Zorlamalı tünel trafiği için şirket içi yerel ağ sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd218-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="fd218-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd218-112">-Profile</span></span>
<span data-ttu-id="fd218-113">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd218-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd218-114">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fd218-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd218-115">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="fd218-115">-VNetName</span></span>
<span data-ttu-id="fd218-116">Sanal ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd218-116">Specifies a virtual network.</span></span>
<span data-ttu-id="fd218-117">Bu cmdlet, bu parametrenin belirttiği sanal ağın Zorlamalı tünel trafiği için VPN ağ geçidinin varsayılan yolunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fd218-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd218-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd218-118">CommonParameters</span></span>
<span data-ttu-id="fd218-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd218-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd218-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd218-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd218-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd218-121">INPUTS</span></span>

## <span data-ttu-id="fd218-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd218-122">OUTPUTS</span></span>

## <span data-ttu-id="fd218-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd218-123">NOTES</span></span>

## <span data-ttu-id="fd218-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd218-124">RELATED LINKS</span></span>

[<span data-ttu-id="fd218-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fd218-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
