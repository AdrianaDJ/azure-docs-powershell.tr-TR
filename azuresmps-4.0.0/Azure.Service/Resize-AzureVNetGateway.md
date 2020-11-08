---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106087"
---
# <span data-ttu-id="8b5f0-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="8b5f0-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="8b5f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5f0-103">VPN ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="8b5f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b5f0-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b5f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5f0-106">**Resize-AzureVNetGateway** cmdlet 'i sanal ağ sanal özel ağ (VPN) ağ geçidini farklı bir SKU 'ya yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="8b5f0-107">Sanal ağ geçidi için geçerli SKU 'Lar varsayılan, standart ve HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="8b5f0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b5f0-108">EXAMPLES</span></span>

### <span data-ttu-id="8b5f0-109">Örnek 1: sanal ağ geçidi için SKU 'YU değiştirme</span><span class="sxs-lookup"><span data-stu-id="8b5f0-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="8b5f0-110">Bu komut, ContosoVN07 adındaki sanal ağın sanal ağ geçidinin SKU 'SU</span><span class="sxs-lookup"><span data-stu-id="8b5f0-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="8b5f0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b5f0-111">PARAMETERS</span></span>

### <span data-ttu-id="8b5f0-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="8b5f0-112">-GatewaySKU</span></span>
<span data-ttu-id="8b5f0-113">Bu cmdlet 'in sanal ağ geçidini yeniden boyutlandırdıkları SKU 'YU belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="8b5f0-114">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8b5f0-114">Valid values are:</span></span> 

- <span data-ttu-id="8b5f0-115">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="8b5f0-115">Default</span></span> 
- <span data-ttu-id="8b5f0-116">Ardından</span><span class="sxs-lookup"><span data-stu-id="8b5f0-116">Standard</span></span> 
- <span data-ttu-id="8b5f0-117">Üst performans</span><span class="sxs-lookup"><span data-stu-id="8b5f0-117">HighPerformance</span></span>

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

### <span data-ttu-id="8b5f0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="8b5f0-118">-Profile</span></span>
<span data-ttu-id="8b5f0-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8b5f0-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b5f0-121">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="8b5f0-121">-VNetName</span></span>
<span data-ttu-id="8b5f0-122">Bu cmdlet 'in sanal ağ ağ geçidini yeniden boyutlandırdıkları sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="8b5f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5f0-123">CommonParameters</span></span>
<span data-ttu-id="8b5f0-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b5f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5f0-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5f0-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b5f0-126">INPUTS</span></span>

## <span data-ttu-id="8b5f0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b5f0-127">OUTPUTS</span></span>

## <span data-ttu-id="8b5f0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b5f0-128">NOTES</span></span>

## <span data-ttu-id="8b5f0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b5f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="8b5f0-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="8b5f0-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="8b5f0-131">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="8b5f0-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="8b5f0-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="8b5f0-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="8b5f0-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="8b5f0-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="8b5f0-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="8b5f0-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


