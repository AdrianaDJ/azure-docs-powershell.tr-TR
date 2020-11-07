---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935524"
---
# <span data-ttu-id="ed1af-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ed1af-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ed1af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed1af-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1af-103">Ağ arabiriminin ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ed1af-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="ed1af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed1af-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed1af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed1af-105">DESCRIPTION</span></span>
<span data-ttu-id="ed1af-106">**Get-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ed1af-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="ed1af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed1af-107">EXAMPLES</span></span>

### <span data-ttu-id="ed1af-108">1: ağ arabiriminin IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="ed1af-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="ed1af-109">İlk komut MyNic adlı bir ağ arabirimini alır ve bunu 1 $nic değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="ed1af-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="ed1af-110">İkinci komut, bu ağ arabiriminin ipconfig1 adındaki IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ed1af-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="ed1af-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed1af-111">PARAMETERS</span></span>

### <span data-ttu-id="ed1af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1af-112">-DefaultProfile</span></span>
<span data-ttu-id="ed1af-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed1af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed1af-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed1af-114">-Name</span></span>
<span data-ttu-id="ed1af-115">Bu cmdlet 'in aldığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed1af-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed1af-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ed1af-116">-NetworkInterface</span></span>
<span data-ttu-id="ed1af-117">Bu cmdlet 'in aldığı ağ IP yapılandırmasını içeren bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed1af-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ed1af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1af-118">CommonParameters</span></span>
<span data-ttu-id="ed1af-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed1af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1af-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1af-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1af-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed1af-121">INPUTS</span></span>

### <span data-ttu-id="ed1af-122">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="ed1af-122">PSNetworkInterface</span></span>
<span data-ttu-id="ed1af-123">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="ed1af-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="ed1af-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed1af-124">OUTPUTS</span></span>

### <span data-ttu-id="ed1af-125">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ed1af-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="ed1af-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed1af-126">NOTES</span></span>
* <span data-ttu-id="ed1af-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="ed1af-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ed1af-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed1af-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed1af-129">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="ed1af-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed1af-130">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="ed1af-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed1af-131">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="ed1af-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ed1af-132">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="ed1af-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


