---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765054"
---
# <span data-ttu-id="72df1-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="72df1-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="72df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72df1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72df1-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72df1-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72df1-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="72df1-104">DESCRIPTION</span></span>

## <span data-ttu-id="72df1-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72df1-105">EXAMPLES</span></span>

### <span data-ttu-id="72df1-106">Örnek 1: sanal ağ eşliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="72df1-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="72df1-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72df1-107">PARAMETERS</span></span>

### <span data-ttu-id="72df1-108">-Force</span><span class="sxs-lookup"><span data-stu-id="72df1-108">-Force</span></span>
<span data-ttu-id="72df1-109">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="72df1-109">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-110">-Ad</span><span class="sxs-lookup"><span data-stu-id="72df1-110">-Name</span></span>
<span data-ttu-id="72df1-111">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="72df1-111">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="72df1-112">-PassThru</span></span>
<span data-ttu-id="72df1-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="72df1-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72df1-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="72df1-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72df1-115">-ResourceGroupName</span></span>
<span data-ttu-id="72df1-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="72df1-116">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="72df1-117">-VirtualNetworkName</span></span>
<span data-ttu-id="72df1-118">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="72df1-118">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="72df1-119">-Confirm</span></span>
<span data-ttu-id="72df1-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72df1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72df1-121">-WhatIf</span></span>
<span data-ttu-id="72df1-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72df1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72df1-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72df1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72df1-124">-DefaultProfile</span></span>
<span data-ttu-id="72df1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72df1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72df1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72df1-126">CommonParameters</span></span>
<span data-ttu-id="72df1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72df1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72df1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72df1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72df1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72df1-129">INPUTS</span></span>

## <span data-ttu-id="72df1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72df1-130">OUTPUTS</span></span>

## <span data-ttu-id="72df1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72df1-131">NOTES</span></span>

## <span data-ttu-id="72df1-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72df1-132">RELATED LINKS</span></span>

