---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106150"
---
# <span data-ttu-id="199a7-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="199a7-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="199a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199a7-102">SYNOPSIS</span></span>
<span data-ttu-id="199a7-103">Bir ağ güvenlik grubunun alt ağdan ilişkisini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="199a7-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="199a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="199a7-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="199a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="199a7-105">DESCRIPTION</span></span>
<span data-ttu-id="199a7-106">**Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet 'ı bir Azure ağ güvenlik grubunu alt ağdan ayırır.</span><span class="sxs-lookup"><span data-stu-id="199a7-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="199a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="199a7-107">EXAMPLES</span></span>

## <span data-ttu-id="199a7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="199a7-108">PARAMETERS</span></span>

### <span data-ttu-id="199a7-109">-Force</span><span class="sxs-lookup"><span data-stu-id="199a7-109">-Force</span></span>
<span data-ttu-id="199a7-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="199a7-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="199a7-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="199a7-111">-Name</span></span>
<span data-ttu-id="199a7-112">Bu cmdlet 'in alt ağla ilişkisi olan ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="199a7-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="199a7-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="199a7-113">-PassThru</span></span>
<span data-ttu-id="199a7-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="199a7-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="199a7-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="199a7-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="199a7-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="199a7-116">-Profile</span></span>
<span data-ttu-id="199a7-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="199a7-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="199a7-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="199a7-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="199a7-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="199a7-119">-SubnetName</span></span>
<span data-ttu-id="199a7-120">Bu cmdlet 'in bir ağ güvenlik grubunun ilişkisini kaldırdıkları alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="199a7-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="199a7-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="199a7-121">-VirtualNetworkName</span></span>
<span data-ttu-id="199a7-122">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="199a7-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="199a7-123">Bu cmdlet, bir ağ güvenlik grubunu sanal ağdaki bu parametrenin belirttiği bir alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="199a7-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="199a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199a7-124">CommonParameters</span></span>
<span data-ttu-id="199a7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="199a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199a7-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="199a7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199a7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="199a7-127">INPUTS</span></span>

## <span data-ttu-id="199a7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="199a7-128">OUTPUTS</span></span>

## <span data-ttu-id="199a7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="199a7-129">NOTES</span></span>

## <span data-ttu-id="199a7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="199a7-130">RELATED LINKS</span></span>

[<span data-ttu-id="199a7-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="199a7-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="199a7-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="199a7-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


