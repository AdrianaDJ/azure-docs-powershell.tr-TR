---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590717"
---
# <span data-ttu-id="61c4a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="61c4a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="61c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="61c4a-103">Sanal Ağ Geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="61c4a-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61c4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61c4a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61c4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="61c4a-106">**Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet 'i sanal ağ geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="61c4a-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="61c4a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61c4a-107">EXAMPLES</span></span>

## <span data-ttu-id="61c4a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61c4a-108">PARAMETERS</span></span>

### <span data-ttu-id="61c4a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="61c4a-109">-Force</span></span>
<span data-ttu-id="61c4a-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="61c4a-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61c4a-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="61c4a-111">-Name</span></span>
<span data-ttu-id="61c4a-112">Sanal ağ geçidi paylaşılan anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c4a-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="61c4a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c4a-113">-ResourceGroupName</span></span>
<span data-ttu-id="61c4a-114">Sanal ağ geçidinin ait olduğu kaynak grubunun adını belirtir</span><span class="sxs-lookup"><span data-stu-id="61c4a-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="61c4a-115">-Değer</span><span class="sxs-lookup"><span data-stu-id="61c4a-115">-Value</span></span>
<span data-ttu-id="61c4a-116">Paylaşılan anahtarın değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c4a-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="61c4a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="61c4a-117">-Confirm</span></span>
<span data-ttu-id="61c4a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61c4a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61c4a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c4a-119">-WhatIf</span></span>
<span data-ttu-id="61c4a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61c4a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c4a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61c4a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61c4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c4a-122">-DefaultProfile</span></span>
<span data-ttu-id="61c4a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61c4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c4a-124">CommonParameters</span></span>
<span data-ttu-id="61c4a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61c4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c4a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c4a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c4a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61c4a-127">INPUTS</span></span>

## <span data-ttu-id="61c4a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61c4a-128">OUTPUTS</span></span>

### <span data-ttu-id="61c4a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61c4a-129">System.String</span></span>

## <span data-ttu-id="61c4a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61c4a-130">NOTES</span></span>

## <span data-ttu-id="61c4a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61c4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="61c4a-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="61c4a-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="61c4a-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="61c4a-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


