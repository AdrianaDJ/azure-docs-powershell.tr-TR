---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106275"
---
# <span data-ttu-id="05ec0-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="05ec0-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="05ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="05ec0-103">Sanal ağ geçidi ile yerel ağ sitesi arasındaki bağlantının önceden paylaşılan anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="05ec0-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="05ec0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05ec0-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="05ec0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="05ec0-106">**Get-AzureVNetGatewayKey** cmdlet 'i sanal ağ geçidi ile yerel ağ sitesi arasındaki bağlantı için önceden paylaşılan anahtarı alır.</span><span class="sxs-lookup"><span data-stu-id="05ec0-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="05ec0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05ec0-107">EXAMPLES</span></span>

## <span data-ttu-id="05ec0-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05ec0-108">PARAMETERS</span></span>

### <span data-ttu-id="05ec0-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="05ec0-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="05ec0-110">Sanal ağ geçidine bağlanan yerel ağ sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05ec0-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="05ec0-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="05ec0-111">-Profile</span></span>
<span data-ttu-id="05ec0-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05ec0-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="05ec0-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="05ec0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05ec0-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="05ec0-114">-VNetName</span></span>
<span data-ttu-id="05ec0-115">Bu cmdlet 'in bağlantılar için paylaşılan anahtarı aldığı sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="05ec0-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="05ec0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ec0-116">CommonParameters</span></span>
<span data-ttu-id="05ec0-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05ec0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ec0-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ec0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ec0-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05ec0-119">INPUTS</span></span>

## <span data-ttu-id="05ec0-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05ec0-120">OUTPUTS</span></span>

## <span data-ttu-id="05ec0-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05ec0-121">NOTES</span></span>

## <span data-ttu-id="05ec0-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05ec0-122">RELATED LINKS</span></span>

[<span data-ttu-id="05ec0-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="05ec0-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


