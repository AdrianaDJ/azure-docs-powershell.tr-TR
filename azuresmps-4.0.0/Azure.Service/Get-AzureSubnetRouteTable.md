---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105542"
---
# <span data-ttu-id="47c41-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="47c41-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="47c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c41-102">SYNOPSIS</span></span>
<span data-ttu-id="47c41-103">Alt ağ için yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="47c41-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="47c41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47c41-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47c41-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47c41-105">DESCRIPTION</span></span>
<span data-ttu-id="47c41-106">**Get-azuyeniden gönderme Netroutetable** cmdlet 'i bir alt ağla ilişkilendirilmiş yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="47c41-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="47c41-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47c41-107">EXAMPLES</span></span>

### <span data-ttu-id="47c41-108">Örnek 1: alt ağın yollarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="47c41-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="47c41-109">Bu komut, ContosoSubnet adlı alt ağla ilişkili yol tablosu adındaki yolları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="47c41-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="47c41-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47c41-110">PARAMETERS</span></span>

### <span data-ttu-id="47c41-111">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="47c41-111">-Detailed</span></span>
<span data-ttu-id="47c41-112">Bu cmdlet 'in alt ağla ilişkili yol tablosundaki yolları görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47c41-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="47c41-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="47c41-113">-Profile</span></span>
<span data-ttu-id="47c41-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47c41-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="47c41-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="47c41-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47c41-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="47c41-116">-SubnetName</span></span>
<span data-ttu-id="47c41-117">Bu cmdlet 'in yol tablosunu aldığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="47c41-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="47c41-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="47c41-118">-VirtualNetworkName</span></span>
<span data-ttu-id="47c41-119">Bu cmdlet 'in yol tablosunu aldığı alt ağı içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47c41-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="47c41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c41-120">CommonParameters</span></span>
<span data-ttu-id="47c41-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47c41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c41-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47c41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c41-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47c41-123">INPUTS</span></span>

## <span data-ttu-id="47c41-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47c41-124">OUTPUTS</span></span>

## <span data-ttu-id="47c41-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47c41-125">NOTES</span></span>

## <span data-ttu-id="47c41-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47c41-126">RELATED LINKS</span></span>

[<span data-ttu-id="47c41-127">Remove-Azuyeniden yönlendirme</span><span class="sxs-lookup"><span data-stu-id="47c41-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="47c41-128">Set-Azuyeniden gönderiliyor Netroutetable</span><span class="sxs-lookup"><span data-stu-id="47c41-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


