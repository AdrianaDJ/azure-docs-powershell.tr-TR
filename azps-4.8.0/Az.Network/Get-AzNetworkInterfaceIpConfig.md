---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266044"
---
# <span data-ttu-id="34f8b-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="34f8b-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="34f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="34f8b-103">Ağ arabiriminin ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="34f8b-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="34f8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34f8b-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="34f8b-106">**Get-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="34f8b-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="34f8b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="34f8b-108">1: ağ arabiriminin IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="34f8b-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="34f8b-109">İlk komut MyNic adlı bir ağ arabirimini alır ve bunu 1 $nic değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="34f8b-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="34f8b-110">İkinci komut, bu ağ arabiriminin ipconfig1 adındaki IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="34f8b-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="34f8b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34f8b-111">PARAMETERS</span></span>

### <span data-ttu-id="34f8b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f8b-112">-DefaultProfile</span></span>
<span data-ttu-id="34f8b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34f8b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f8b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="34f8b-114">-Name</span></span>
<span data-ttu-id="34f8b-115">Bu cmdlet 'in aldığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f8b-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f8b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="34f8b-116">-NetworkInterface</span></span>
<span data-ttu-id="34f8b-117">Bu cmdlet 'in aldığı ağ IP yapılandırmasını içeren bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f8b-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="34f8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f8b-118">CommonParameters</span></span>
<span data-ttu-id="34f8b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34f8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f8b-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34f8b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f8b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34f8b-121">INPUTS</span></span>

### <span data-ttu-id="34f8b-122">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="34f8b-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="34f8b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34f8b-123">OUTPUTS</span></span>

### <span data-ttu-id="34f8b-124">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="34f8b-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="34f8b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34f8b-125">NOTES</span></span>
* <span data-ttu-id="34f8b-126">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="34f8b-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="34f8b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34f8b-127">RELATED LINKS</span></span>

[<span data-ttu-id="34f8b-128">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="34f8b-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="34f8b-129">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="34f8b-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="34f8b-130">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="34f8b-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="34f8b-131">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="34f8b-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


