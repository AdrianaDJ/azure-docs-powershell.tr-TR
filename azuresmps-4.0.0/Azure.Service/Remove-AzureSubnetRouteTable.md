---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106456"
---
# <span data-ttu-id="42f1c-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="42f1c-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="42f1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="42f1c-103">Alt ağdan yol tablosu ilişkisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42f1c-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="42f1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42f1c-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42f1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="42f1c-106">**Remove-azuyeniden yönlendirme Netroutetable** cmdlet 'i, alt ağdan yol tablosu ilişkilendirmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42f1c-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="42f1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42f1c-107">EXAMPLES</span></span>

### <span data-ttu-id="42f1c-108">Örnek 1: yol tablosuyla alt ağ arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="42f1c-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="42f1c-109">Bu komut, PublicRouteTable adlı yönlendirme tablosunun, ContosoSubnet adlı alt ağla ilişkisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42f1c-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="42f1c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42f1c-110">PARAMETERS</span></span>

### <span data-ttu-id="42f1c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="42f1c-111">-Force</span></span>
<span data-ttu-id="42f1c-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="42f1c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42f1c-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="42f1c-113">-PassThru</span></span>
<span data-ttu-id="42f1c-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="42f1c-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="42f1c-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="42f1c-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42f1c-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="42f1c-116">-Profile</span></span>
<span data-ttu-id="42f1c-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42f1c-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="42f1c-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="42f1c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42f1c-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="42f1c-119">-SubnetName</span></span>
<span data-ttu-id="42f1c-120">Bu cmdlet 'in yol tablosunu kaldırdığı alt ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="42f1c-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="42f1c-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="42f1c-121">-VirtualNetworkName</span></span>
<span data-ttu-id="42f1c-122">Bu cmdlet 'in yol tablosunu kaldırdığı alt ağı içeren sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42f1c-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="42f1c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f1c-123">CommonParameters</span></span>
<span data-ttu-id="42f1c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42f1c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f1c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f1c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f1c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42f1c-126">INPUTS</span></span>

## <span data-ttu-id="42f1c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42f1c-127">OUTPUTS</span></span>

## <span data-ttu-id="42f1c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42f1c-128">NOTES</span></span>

## <span data-ttu-id="42f1c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42f1c-129">RELATED LINKS</span></span>

[<span data-ttu-id="42f1c-130">Get-Azuyeniden gönderme Netroutetable</span><span class="sxs-lookup"><span data-stu-id="42f1c-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="42f1c-131">Set-Azuyeniden gönderiliyor Netroutetable</span><span class="sxs-lookup"><span data-stu-id="42f1c-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


