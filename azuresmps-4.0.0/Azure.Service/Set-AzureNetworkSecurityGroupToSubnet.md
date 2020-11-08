---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105829"
---
# <span data-ttu-id="d9d9f-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="d9d9f-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="d9d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d9f-103">Ağ güvenlik grubunu alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="d9d9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9d9f-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9d9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d9f-106">**Set-AzureNetworkSecurityGroupToSubnet** cmdlet 'ı bir Azure ağ güvenlik grubunu alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="d9d9f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9d9f-107">EXAMPLES</span></span>

## <span data-ttu-id="d9d9f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9d9f-108">PARAMETERS</span></span>

### <span data-ttu-id="d9d9f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="d9d9f-109">-Force</span></span>
<span data-ttu-id="d9d9f-110">Bu cmdlet 'in alt ağdan önceki bir ağ güvenlik grubunun kaldırılmasını onaylamanızı istemez.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="d9d9f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9d9f-111">-Name</span></span>
<span data-ttu-id="d9d9f-112">Bu cmdlet 'in alt ağla ilişkilendiğinden ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="d9d9f-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d9d9f-113">-PassThru</span></span>
<span data-ttu-id="d9d9f-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d9d9f-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9d9f-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9d9f-116">-Profile</span></span>
<span data-ttu-id="d9d9f-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d9d9f-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9d9f-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d9d9f-119">-SubnetName</span></span>
<span data-ttu-id="d9d9f-120">Bu cmdlet 'in bir ağ güvenlik grubunu ilişkilendiğinde alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="d9d9f-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d9d9f-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d9d9f-122">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="d9d9f-123">Bu cmdlet, bir ağ güvenlik grubunu sanal ağdaki bu parametrenin belirttiği alt ağla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9d9f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d9f-124">CommonParameters</span></span>
<span data-ttu-id="d9d9f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9d9f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d9f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d9f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d9f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9d9f-127">INPUTS</span></span>

## <span data-ttu-id="d9d9f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9d9f-128">OUTPUTS</span></span>

## <span data-ttu-id="d9d9f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9d9f-129">NOTES</span></span>

## <span data-ttu-id="d9d9f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9d9f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9d9f-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="d9d9f-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="d9d9f-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="d9d9f-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


