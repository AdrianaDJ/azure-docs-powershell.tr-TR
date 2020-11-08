---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 784374b620af09b00f460ff5c50d0a08baa46233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104019"
---
# <span data-ttu-id="1e460-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e460-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="1e460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e460-102">SYNOPSIS</span></span>
<span data-ttu-id="1e460-103">Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e460-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="1e460-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e460-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e460-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e460-105">DESCRIPTION</span></span>
<span data-ttu-id="1e460-106">**Remove-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e460-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="1e460-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e460-107">EXAMPLES</span></span>

### <span data-ttu-id="1e460-108">1: ağ arabiriminden IP yapılandırmasını silme</span><span class="sxs-lookup"><span data-stu-id="1e460-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="1e460-109">İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1e460-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="1e460-110">İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e460-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="1e460-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e460-111">PARAMETERS</span></span>

### <span data-ttu-id="1e460-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e460-112">-DefaultProfile</span></span>
<span data-ttu-id="1e460-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e460-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e460-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e460-114">-Name</span></span>
<span data-ttu-id="1e460-115">Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e460-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e460-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e460-116">-NetworkInterface</span></span>
<span data-ttu-id="1e460-117">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e460-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="1e460-118">Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="1e460-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e460-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e460-119">CommonParameters</span></span>
<span data-ttu-id="1e460-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e460-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e460-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e460-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e460-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e460-122">INPUTS</span></span>

### <span data-ttu-id="1e460-123">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="1e460-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="1e460-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e460-124">OUTPUTS</span></span>

### <span data-ttu-id="1e460-125">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="1e460-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="1e460-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e460-126">NOTES</span></span>
* <span data-ttu-id="1e460-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="1e460-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1e460-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e460-128">RELATED LINKS</span></span>

[<span data-ttu-id="1e460-129">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="1e460-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1e460-130">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="1e460-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1e460-131">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="1e460-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1e460-132">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="1e460-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


