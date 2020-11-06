---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: c912d32c39380ee3d653fa228632a4d01f0e3049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590142"
---
# <span data-ttu-id="8ac34-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac34-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="8ac34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac34-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac34-103">Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ac34-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ac34-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ac34-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac34-106">**Remove-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ac34-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="8ac34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ac34-107">EXAMPLES</span></span>

### <span data-ttu-id="8ac34-108">1: ağ arabiriminden IP yapılandırmasını silme</span><span class="sxs-lookup"><span data-stu-id="8ac34-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="8ac34-109">İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="8ac34-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="8ac34-110">İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ac34-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="8ac34-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ac34-111">PARAMETERS</span></span>

### <span data-ttu-id="8ac34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac34-112">-DefaultProfile</span></span>
<span data-ttu-id="8ac34-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ac34-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac34-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ac34-114">-Name</span></span>
<span data-ttu-id="8ac34-115">Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ac34-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="8ac34-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8ac34-116">-NetworkInterface</span></span>
<span data-ttu-id="8ac34-117">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ac34-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="8ac34-118">Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="8ac34-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="8ac34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac34-119">CommonParameters</span></span>
<span data-ttu-id="8ac34-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ac34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac34-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac34-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac34-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ac34-122">INPUTS</span></span>

### <span data-ttu-id="8ac34-123">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="8ac34-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="8ac34-124">Parametreler: Ağarabirimi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ac34-124">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="8ac34-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ac34-125">OUTPUTS</span></span>

### <span data-ttu-id="8ac34-126">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="8ac34-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8ac34-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ac34-127">NOTES</span></span>
* <span data-ttu-id="8ac34-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="8ac34-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8ac34-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ac34-129">RELATED LINKS</span></span>

[<span data-ttu-id="8ac34-130">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8ac34-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8ac34-131">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8ac34-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8ac34-132">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8ac34-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8ac34-133">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8ac34-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


