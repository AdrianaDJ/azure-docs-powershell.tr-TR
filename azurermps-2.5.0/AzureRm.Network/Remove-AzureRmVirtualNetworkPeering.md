---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940029"
---
# <span data-ttu-id="02a79-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="02a79-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="02a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a79-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a79-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02a79-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02a79-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="02a79-104">DESCRIPTION</span></span>

## <span data-ttu-id="02a79-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02a79-105">EXAMPLES</span></span>

### <span data-ttu-id="02a79-106">Örnek 1: sanal ağ eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="02a79-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="02a79-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02a79-107">PARAMETERS</span></span>

### <span data-ttu-id="02a79-108">-Iş</span><span class="sxs-lookup"><span data-stu-id="02a79-108">-AsJob</span></span>
<span data-ttu-id="02a79-109">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02a79-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02a79-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a79-110">-DefaultProfile</span></span>
<span data-ttu-id="02a79-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02a79-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a79-112">-Force</span><span class="sxs-lookup"><span data-stu-id="02a79-112">-Force</span></span>
<span data-ttu-id="02a79-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="02a79-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02a79-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="02a79-114">-Name</span></span>
<span data-ttu-id="02a79-115">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="02a79-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="02a79-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02a79-116">-PassThru</span></span>
<span data-ttu-id="02a79-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="02a79-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02a79-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="02a79-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02a79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a79-119">-ResourceGroupName</span></span>
<span data-ttu-id="02a79-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="02a79-120">The resource group name</span></span>

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

### <span data-ttu-id="02a79-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="02a79-121">-VirtualNetworkName</span></span>
<span data-ttu-id="02a79-122">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="02a79-122">The virtual network name.</span></span>

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

### <span data-ttu-id="02a79-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="02a79-123">-Confirm</span></span>
<span data-ttu-id="02a79-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02a79-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a79-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a79-125">-WhatIf</span></span>
<span data-ttu-id="02a79-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02a79-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a79-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02a79-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a79-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a79-128">CommonParameters</span></span>
<span data-ttu-id="02a79-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02a79-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a79-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a79-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a79-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02a79-131">INPUTS</span></span>

## <span data-ttu-id="02a79-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02a79-132">OUTPUTS</span></span>

## <span data-ttu-id="02a79-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02a79-133">NOTES</span></span>

## <span data-ttu-id="02a79-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02a79-134">RELATED LINKS</span></span>

