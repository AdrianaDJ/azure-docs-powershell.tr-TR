---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106287"
---
# <span data-ttu-id="e71ad-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="e71ad-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="e71ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e71ad-103">Bir Azure sanal ağıyla bağlantı alır.</span><span class="sxs-lookup"><span data-stu-id="e71ad-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="e71ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e71ad-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e71ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e71ad-105">DESCRIPTION</span></span>
<span data-ttu-id="e71ad-106">**Get-AzureVNetConnection** cmdlet 'ı bir Azure sanal ağına tüm etkin sanal özel ağ (VPN) bağlantılarını belirten bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e71ad-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="e71ad-107">VPN bağlantıları, şirket içi siteden siteye VPN ve sanal ağı sanal ağ bağlantılarına ekler.</span><span class="sxs-lookup"><span data-stu-id="e71ad-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="e71ad-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e71ad-108">EXAMPLES</span></span>

## <span data-ttu-id="e71ad-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e71ad-109">PARAMETERS</span></span>

### <span data-ttu-id="e71ad-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="e71ad-110">-Profile</span></span>
<span data-ttu-id="e71ad-111">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e71ad-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e71ad-112">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e71ad-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e71ad-113">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="e71ad-113">-VNetName</span></span>
<span data-ttu-id="e71ad-114">Bu cmdlet 'in bağlantıları döndürdüğü sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e71ad-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="e71ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71ad-115">CommonParameters</span></span>
<span data-ttu-id="e71ad-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e71ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71ad-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71ad-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71ad-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e71ad-118">INPUTS</span></span>

## <span data-ttu-id="e71ad-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e71ad-119">OUTPUTS</span></span>

## <span data-ttu-id="e71ad-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e71ad-120">NOTES</span></span>

## <span data-ttu-id="e71ad-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e71ad-121">RELATED LINKS</span></span>

