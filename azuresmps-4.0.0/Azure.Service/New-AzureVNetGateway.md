---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106187"
---
# <span data-ttu-id="1343d-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1343d-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="1343d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1343d-102">SYNOPSIS</span></span>
<span data-ttu-id="1343d-103">Sanal ağda VPN ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1343d-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="1343d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1343d-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1343d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1343d-105">DESCRIPTION</span></span>
<span data-ttu-id="1343d-106">**New-AzureVNetGateway** cmdlet 'i sanal bir ağda sanal özel ağ (VPN) ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1343d-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="1343d-107">Ayrıca, ağ geçidi SKU 'yu varsayılan, standart veya HighPerformance olarak da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1343d-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="1343d-108">Türü (StaticRouting veya Dynamıuting) belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1343d-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="1343d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1343d-109">EXAMPLES</span></span>

### <span data-ttu-id="1343d-110">Örnek 1: sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1343d-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="1343d-111">Bu komut, ContosoVN07 adındaki sanal ağda sanal ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1343d-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="1343d-112">Ağ Geçidi varsayılan SKU.</span><span class="sxs-lookup"><span data-stu-id="1343d-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="1343d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1343d-113">PARAMETERS</span></span>

### <span data-ttu-id="1343d-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="1343d-114">-GatewaySKU</span></span>
<span data-ttu-id="1343d-115">Bu cmdlet 'in oluşturduğu sanal ağ geçidinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1343d-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="1343d-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1343d-116">Valid values are:</span></span> 

- <span data-ttu-id="1343d-117">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="1343d-117">Default</span></span> 
- <span data-ttu-id="1343d-118">Ardından</span><span class="sxs-lookup"><span data-stu-id="1343d-118">Standard</span></span> 
- <span data-ttu-id="1343d-119">Üst performans</span><span class="sxs-lookup"><span data-stu-id="1343d-119">HighPerformance</span></span>

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

### <span data-ttu-id="1343d-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="1343d-120">-GatewayType</span></span>
<span data-ttu-id="1343d-121">Bu cmdlet 'in oluşturduğu ağ geçidi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1343d-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="1343d-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1343d-122">Valid values are:</span></span> 

- <span data-ttu-id="1343d-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="1343d-123">StaticRouting</span></span> 
- <span data-ttu-id="1343d-124">Dynamikrokapatma</span><span class="sxs-lookup"><span data-stu-id="1343d-124">DynamicRouting</span></span>

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

### <span data-ttu-id="1343d-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="1343d-125">-Profile</span></span>
<span data-ttu-id="1343d-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1343d-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1343d-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1343d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1343d-128">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="1343d-128">-VNetName</span></span>
<span data-ttu-id="1343d-129">Bu cmdlet 'in sanal ağ geçidi eklediği sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1343d-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="1343d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1343d-130">CommonParameters</span></span>
<span data-ttu-id="1343d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1343d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1343d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1343d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1343d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1343d-133">INPUTS</span></span>

## <span data-ttu-id="1343d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1343d-134">OUTPUTS</span></span>

## <span data-ttu-id="1343d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1343d-135">NOTES</span></span>

## <span data-ttu-id="1343d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1343d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1343d-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1343d-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="1343d-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1343d-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="1343d-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1343d-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="1343d-140">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="1343d-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="1343d-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="1343d-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


