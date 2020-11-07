---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8d8254b5002edcf40b0807e296ab680ea32ca10e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764811"
---
# <span data-ttu-id="4e444-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4e444-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="4e444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e444-102">SYNOPSIS</span></span>
<span data-ttu-id="4e444-103">Ağ arabiriminin ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e444-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e444-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e444-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e444-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e444-105">DESCRIPTION</span></span>
<span data-ttu-id="4e444-106">**Get-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e444-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="4e444-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e444-107">EXAMPLES</span></span>

### <span data-ttu-id="4e444-108">1: ağ arabiriminin IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="4e444-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="4e444-109">İlk komut MyNic adlı bir ağ arabirimini alır ve bunu 1 $nic değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="4e444-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="4e444-110">İkinci komut, bu ağ arabiriminin ipconfig1 adındaki IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e444-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="4e444-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e444-111">PARAMETERS</span></span>

### <span data-ttu-id="4e444-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e444-112">-DefaultProfile</span></span>
<span data-ttu-id="4e444-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e444-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e444-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e444-114">-Name</span></span>
<span data-ttu-id="4e444-115">Bu cmdlet 'in aldığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e444-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e444-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4e444-116">-NetworkInterface</span></span>
<span data-ttu-id="4e444-117">Bu cmdlet 'in aldığı ağ IP yapılandırmasını içeren bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e444-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e444-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e444-118">CommonParameters</span></span>
<span data-ttu-id="4e444-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e444-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e444-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e444-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e444-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e444-121">INPUTS</span></span>

### <span data-ttu-id="4e444-122">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="4e444-122">PSNetworkInterface</span></span>
<span data-ttu-id="4e444-123">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="4e444-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="4e444-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e444-124">OUTPUTS</span></span>

### <span data-ttu-id="4e444-125">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="4e444-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="4e444-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e444-126">NOTES</span></span>
* <span data-ttu-id="4e444-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4e444-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4e444-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e444-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e444-129">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4e444-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4e444-130">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4e444-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4e444-131">Remove-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4e444-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4e444-132">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4e444-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


