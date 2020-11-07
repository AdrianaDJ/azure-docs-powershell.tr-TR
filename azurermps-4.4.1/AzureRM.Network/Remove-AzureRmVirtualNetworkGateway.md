---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 401fcbd5fca9fc0251e4de0fb7843fb95c1c122d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593523"
---
# <span data-ttu-id="4b53f-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4b53f-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="4b53f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b53f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b53f-103">Sanal ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="4b53f-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b53f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b53f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b53f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b53f-105">DESCRIPTION</span></span>
<span data-ttu-id="4b53f-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="4b53f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="4b53f-107">**Get-AzureRmVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b53f-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4b53f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b53f-108">EXAMPLES</span></span>

### <span data-ttu-id="4b53f-109">1: sanal ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="4b53f-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="4b53f-110">Sanal ağ geçidinin, "myRG" kaynak grubundaki "myGateway" adıyla</span><span class="sxs-lookup"><span data-stu-id="4b53f-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="4b53f-111">Not: **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak sanal ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4b53f-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="4b53f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b53f-112">PARAMETERS</span></span>

### <span data-ttu-id="4b53f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4b53f-113">-Force</span></span>
<span data-ttu-id="4b53f-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4b53f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b53f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b53f-115">-Name</span></span>
<span data-ttu-id="4b53f-116">Bu cmdlet 'in kaldırdığı sanal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b53f-116">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b53f-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4b53f-117">-PassThru</span></span>
<span data-ttu-id="4b53f-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b53f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4b53f-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4b53f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4b53f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b53f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4b53f-121">Sanal ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b53f-121">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="4b53f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b53f-122">-Confirm</span></span>
<span data-ttu-id="4b53f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b53f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b53f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b53f-124">-WhatIf</span></span>
<span data-ttu-id="4b53f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b53f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b53f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b53f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b53f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b53f-127">-DefaultProfile</span></span>
<span data-ttu-id="4b53f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b53f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b53f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b53f-129">CommonParameters</span></span>
<span data-ttu-id="4b53f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b53f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b53f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b53f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b53f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b53f-132">INPUTS</span></span>

## <span data-ttu-id="4b53f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b53f-133">OUTPUTS</span></span>

## <span data-ttu-id="4b53f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b53f-134">NOTES</span></span>

## <span data-ttu-id="4b53f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b53f-135">RELATED LINKS</span></span>
