---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105812"
---
# <span data-ttu-id="86352-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="86352-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="86352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86352-102">SYNOPSIS</span></span>
<span data-ttu-id="86352-103">Yol tablosunu alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="86352-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="86352-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86352-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86352-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="86352-105">DESCRIPTION</span></span>
<span data-ttu-id="86352-106">**Set-azuyeniden** yönlendirme, yol tablosunu bir alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="86352-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="86352-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86352-107">EXAMPLES</span></span>

### <span data-ttu-id="86352-108">Örnek 1: yol tablosunu alt ağla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="86352-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="86352-109">Bu komut, PublicRouteTable adlı yol tablosunu ContosoSubnet adlı alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="86352-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="86352-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86352-110">PARAMETERS</span></span>

### <span data-ttu-id="86352-111">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="86352-111">-PassThru</span></span>
<span data-ttu-id="86352-112">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="86352-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86352-113">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="86352-113">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86352-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="86352-114">-Profile</span></span>
<span data-ttu-id="86352-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86352-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86352-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="86352-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86352-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="86352-117">-RouteTableName</span></span>
<span data-ttu-id="86352-118">Bu cmdlet 'in bir alt ağla ilişkilenmesi gereken yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86352-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="86352-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="86352-119">-SubnetName</span></span>
<span data-ttu-id="86352-120">Bu cmdlet 'in yol tablosunu ilişkilenmesi için alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="86352-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="86352-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="86352-121">-VirtualNetworkName</span></span>
<span data-ttu-id="86352-122">Bu cmdlet 'in yol tablosunu ilişkilendirdiğinden alt ağı içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86352-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="86352-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86352-123">CommonParameters</span></span>
<span data-ttu-id="86352-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86352-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86352-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86352-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86352-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86352-126">INPUTS</span></span>

## <span data-ttu-id="86352-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86352-127">OUTPUTS</span></span>

## <span data-ttu-id="86352-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86352-128">NOTES</span></span>

## <span data-ttu-id="86352-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86352-129">RELATED LINKS</span></span>

[<span data-ttu-id="86352-130">Get-Azuyeniden gönderme Netroutetable</span><span class="sxs-lookup"><span data-stu-id="86352-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="86352-131">Remove-Azuyeniden yönlendirme</span><span class="sxs-lookup"><span data-stu-id="86352-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
