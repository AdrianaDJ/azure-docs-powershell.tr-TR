---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: d532bbee77d028afb4af441dd511deafa6ebc016
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760146"
---
# <span data-ttu-id="fe7f7-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe7f7-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="fe7f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7f7-103">Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="fe7f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe7f7-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe7f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe7f7-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7f7-106">**Remove-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="fe7f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe7f7-107">EXAMPLES</span></span>

### <span data-ttu-id="fe7f7-108">1: ağ arabiriminden IP yapılandırmasını silme</span><span class="sxs-lookup"><span data-stu-id="fe7f7-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="fe7f7-109">İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="fe7f7-110">İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="fe7f7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe7f7-111">PARAMETERS</span></span>

### <span data-ttu-id="fe7f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7f7-112">-DefaultProfile</span></span>
<span data-ttu-id="fe7f7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe7f7-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe7f7-114">-Name</span></span>
<span data-ttu-id="fe7f7-115">Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="fe7f7-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fe7f7-116">-NetworkInterface</span></span>
<span data-ttu-id="fe7f7-117">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="fe7f7-118">Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="fe7f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7f7-119">CommonParameters</span></span>
<span data-ttu-id="fe7f7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7f7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7f7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7f7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe7f7-122">INPUTS</span></span>

### <span data-ttu-id="fe7f7-123">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="fe7f7-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fe7f7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe7f7-124">OUTPUTS</span></span>

### <span data-ttu-id="fe7f7-125">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="fe7f7-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fe7f7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe7f7-126">NOTES</span></span>
* <span data-ttu-id="fe7f7-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="fe7f7-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe7f7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe7f7-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe7f7-129">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="fe7f7-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fe7f7-130">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="fe7f7-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fe7f7-131">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="fe7f7-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fe7f7-132">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="fe7f7-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


