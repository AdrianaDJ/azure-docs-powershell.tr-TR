---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935285"
---
# <span data-ttu-id="d7c30-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7c30-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d7c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c30-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c30-103">Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7c30-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="d7c30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7c30-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7c30-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c30-106">**Remove-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7c30-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="d7c30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7c30-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c30-108">1: ağ arabiriminden IP yapılandırmasını silme</span><span class="sxs-lookup"><span data-stu-id="d7c30-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="d7c30-109">İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d7c30-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="d7c30-110">İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7c30-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="d7c30-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7c30-111">PARAMETERS</span></span>

### <span data-ttu-id="d7c30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c30-112">-DefaultProfile</span></span>
<span data-ttu-id="d7c30-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7c30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c30-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7c30-114">-Name</span></span>
<span data-ttu-id="d7c30-115">Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7c30-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="d7c30-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7c30-116">-NetworkInterface</span></span>
<span data-ttu-id="d7c30-117">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7c30-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d7c30-118">Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="d7c30-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c30-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c30-119">CommonParameters</span></span>
<span data-ttu-id="d7c30-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7c30-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c30-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c30-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c30-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7c30-122">INPUTS</span></span>

### <span data-ttu-id="d7c30-123">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d7c30-123">PSNetworkInterface</span></span>
<span data-ttu-id="d7c30-124">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="d7c30-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d7c30-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7c30-125">OUTPUTS</span></span>

### <span data-ttu-id="d7c30-126">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d7c30-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d7c30-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7c30-127">NOTES</span></span>
* <span data-ttu-id="d7c30-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="d7c30-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d7c30-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7c30-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7c30-130">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d7c30-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d7c30-131">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d7c30-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d7c30-132">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d7c30-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d7c30-133">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d7c30-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


