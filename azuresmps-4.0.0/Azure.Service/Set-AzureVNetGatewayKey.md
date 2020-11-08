---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105810"
---
# <span data-ttu-id="c5889-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c5889-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="c5889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5889-102">SYNOPSIS</span></span>
<span data-ttu-id="c5889-103">Azure VPN ağ geçidi ve yerel ağ sitesi arasındaki bağlantı için önceden paylaşılan anahtarı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c5889-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="c5889-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5889-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5889-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5889-105">DESCRIPTION</span></span>
<span data-ttu-id="c5889-106">**Set-AzureVNetGatewayKey** cmdlet 'i Azure sanal özel ağ (VPN) ağ geçidi ile şirket içi yerel ağ sitesi arasındaki bağlantı için önceden paylaşılan anahtarı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c5889-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="c5889-107">Anahtar, yerel ağ sitesinin ağ geçidinde yapılandırılan anahtarla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="c5889-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="c5889-108">Anahtarlar eşleşmezse bağlantı kuramaz.</span><span class="sxs-lookup"><span data-stu-id="c5889-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="c5889-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5889-109">EXAMPLES</span></span>

## <span data-ttu-id="c5889-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5889-110">PARAMETERS</span></span>

### <span data-ttu-id="c5889-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="c5889-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="c5889-112">Sanal ağ geçidine bağlanan yerel ağ sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5889-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="c5889-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5889-113">-Profile</span></span>
<span data-ttu-id="c5889-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5889-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c5889-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c5889-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5889-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c5889-116">-SharedKey</span></span>
<span data-ttu-id="c5889-117">VPN ağ geçidine atanacak paylaşılan anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5889-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="c5889-118">Değer, 128 karakterden uzun olmayan alfasayısal bir dize olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c5889-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="c5889-119">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="c5889-119">-VNetName</span></span>
<span data-ttu-id="c5889-120">Bu cmdlet 'in bağlantı için paylaşılan anahtarı ayarladığı sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5889-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="c5889-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5889-121">CommonParameters</span></span>
<span data-ttu-id="c5889-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5889-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5889-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5889-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5889-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5889-124">INPUTS</span></span>

## <span data-ttu-id="c5889-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5889-125">OUTPUTS</span></span>

## <span data-ttu-id="c5889-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5889-126">NOTES</span></span>

## <span data-ttu-id="c5889-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5889-127">RELATED LINKS</span></span>

[<span data-ttu-id="c5889-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c5889-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


