---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105823"
---
# <span data-ttu-id="23b7d-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="23b7d-101">Set-AzureRoute</span></span>

## <span data-ttu-id="23b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="23b7d-103">Yol tablosunda bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23b7d-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="23b7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23b7d-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23b7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="23b7d-106">**Set-AzureRoute** cmdlet 'i, yol tablosunda bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23b7d-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="23b7d-107">Yeni yol, yol tablosuyla ilişkilendirilmiş sanal makinelerde hemen hemen gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="23b7d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23b7d-108">EXAMPLES</span></span>

### <span data-ttu-id="23b7d-109">Örnek 1: sonraki atlama rotası sanal bir gereç ekleme</span><span class="sxs-lookup"><span data-stu-id="23b7d-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="23b7d-110">Bu komut, belirtilen konumda ApplianceRouteTable adlı bir yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23b7d-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="23b7d-111">Komut bu yol tablosunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="23b7d-112">Geçerli cmdlet, VirtualAppliance sonraki atlama türü olan ApplianceRoute03 adlı bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="23b7d-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="23b7d-113">Komut sonraki atlama IP adresini ve yolun adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="23b7d-114">Örnek 2: bir Internet sonraki atlama yolunu ekleme</span><span class="sxs-lookup"><span data-stu-id="23b7d-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="23b7d-115">Bu komut, ApplianceRouteTable adlı bir yol tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="23b7d-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="23b7d-116">Komut bu yol tablosunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="23b7d-117">Geçerli cmdlet, ınternetroute adlı bir Internet sonraki atlama türüdür.</span><span class="sxs-lookup"><span data-stu-id="23b7d-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="23b7d-118">Komut, yolun adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="23b7d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23b7d-119">PARAMETERS</span></span>

### <span data-ttu-id="23b7d-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="23b7d-120">-AddressPrefix</span></span>
<span data-ttu-id="23b7d-121">Yeni yol için bir adres öneki belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="23b7d-122">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="23b7d-122">-NextHopIpAddress</span></span>
<span data-ttu-id="23b7d-123">Bu rotayı kullanan trafiğin sonraki atlaması olan gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="23b7d-124">*Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda bu değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="23b7d-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b7d-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="23b7d-125">-NextHopType</span></span>
<span data-ttu-id="23b7d-126">Bu rotayı kullanan trafik için sonraki atlama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="23b7d-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="23b7d-127">Valid values are:</span></span> 

- <span data-ttu-id="23b7d-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="23b7d-128">VPNGateway</span></span>
- <span data-ttu-id="23b7d-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="23b7d-129">VNETLocal</span></span>
- <span data-ttu-id="23b7d-130">İnternete</span><span class="sxs-lookup"><span data-stu-id="23b7d-130">Internet</span></span>
- <span data-ttu-id="23b7d-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="23b7d-131">VirtualAppliance</span></span>
- <span data-ttu-id="23b7d-132">Sonlandırılmış</span><span class="sxs-lookup"><span data-stu-id="23b7d-132">Null</span></span>

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

### <span data-ttu-id="23b7d-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="23b7d-133">-Profile</span></span>
<span data-ttu-id="23b7d-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="23b7d-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="23b7d-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23b7d-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="23b7d-136">-RouteName</span></span>
<span data-ttu-id="23b7d-137">Bu cmdlet 'in eklediği yeni yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="23b7d-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="23b7d-138">-RouteTable</span></span>
<span data-ttu-id="23b7d-139">Bu cmdlet 'in yeni yolu eklediği yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="23b7d-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23b7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b7d-140">CommonParameters</span></span>
<span data-ttu-id="23b7d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23b7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b7d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b7d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b7d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23b7d-143">INPUTS</span></span>

## <span data-ttu-id="23b7d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23b7d-144">OUTPUTS</span></span>

## <span data-ttu-id="23b7d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23b7d-145">NOTES</span></span>

## <span data-ttu-id="23b7d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23b7d-146">RELATED LINKS</span></span>

[<span data-ttu-id="23b7d-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="23b7d-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


