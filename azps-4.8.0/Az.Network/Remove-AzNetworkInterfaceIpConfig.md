---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265941"
---
# <span data-ttu-id="87e14-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87e14-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="87e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e14-102">SYNOPSIS</span></span>
<span data-ttu-id="87e14-103">Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87e14-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="87e14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87e14-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87e14-105">DESCRIPTION</span></span>
<span data-ttu-id="87e14-106">**Remove-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87e14-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="87e14-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87e14-107">EXAMPLES</span></span>

### <span data-ttu-id="87e14-108">Örnek 1: ağ arabiriminden IP yapılandırmasını silme</span><span class="sxs-lookup"><span data-stu-id="87e14-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="87e14-109">İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="87e14-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="87e14-110">İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87e14-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="87e14-111">Üçüncü komut ağ arabiriminde yapılan değişiklikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="87e14-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="87e14-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87e14-112">PARAMETERS</span></span>

### <span data-ttu-id="87e14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e14-113">-DefaultProfile</span></span>
<span data-ttu-id="87e14-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87e14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87e14-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="87e14-115">-Name</span></span>
<span data-ttu-id="87e14-116">Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87e14-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="87e14-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87e14-117">-NetworkInterface</span></span>
<span data-ttu-id="87e14-118">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="87e14-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="87e14-119">Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="87e14-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="87e14-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e14-120">CommonParameters</span></span>
<span data-ttu-id="87e14-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87e14-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e14-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e14-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e14-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87e14-123">INPUTS</span></span>

### <span data-ttu-id="87e14-124">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="87e14-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="87e14-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87e14-125">OUTPUTS</span></span>

### <span data-ttu-id="87e14-126">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="87e14-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="87e14-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87e14-127">NOTES</span></span>
* <span data-ttu-id="87e14-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="87e14-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="87e14-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87e14-129">RELATED LINKS</span></span>

[<span data-ttu-id="87e14-130">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="87e14-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87e14-131">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="87e14-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87e14-132">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="87e14-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87e14-133">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="87e14-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


