---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106276"
---
# <span data-ttu-id="5b11b-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5b11b-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="5b11b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b11b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b11b-103">Sanal ağ geçidi ile yerel ağ sitesi arasındaki bağlantının IPSec parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b11b-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="5b11b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b11b-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5b11b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b11b-105">DESCRIPTION</span></span>
<span data-ttu-id="5b11b-106">**Get-AzureVNetGatewayIPsecParameters** cmdlet 'i sanal ağ geçidi ile yerel bir ağ sitesi arasındaki bağlantının geçerli Internet Protokolü güvenliğini (IPSec) ve Internet Anahtar DEĞIŞIMI (IKE) parametrelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b11b-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="5b11b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b11b-107">EXAMPLES</span></span>

## <span data-ttu-id="5b11b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b11b-108">PARAMETERS</span></span>

### <span data-ttu-id="5b11b-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="5b11b-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="5b11b-110">Sanal ağ geçidine bağlanan yerel ağ sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b11b-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="5b11b-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b11b-111">-Profile</span></span>
<span data-ttu-id="5b11b-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b11b-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5b11b-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5b11b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b11b-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="5b11b-114">-VNetName</span></span>
<span data-ttu-id="5b11b-115">Bu cmdlet 'in bağlantı için IPSec parametrelerini aldığı sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b11b-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="5b11b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b11b-116">CommonParameters</span></span>
<span data-ttu-id="5b11b-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b11b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b11b-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b11b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b11b-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b11b-119">INPUTS</span></span>

## <span data-ttu-id="5b11b-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b11b-120">OUTPUTS</span></span>

## <span data-ttu-id="5b11b-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b11b-121">NOTES</span></span>

## <span data-ttu-id="5b11b-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b11b-122">RELATED LINKS</span></span>

[<span data-ttu-id="5b11b-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="5b11b-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


