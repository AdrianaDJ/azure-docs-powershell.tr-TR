---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: eb88be102f390d9e94ba938eeb6d116af6a79fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918391"
---
# <span data-ttu-id="5f62a-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5f62a-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="5f62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f62a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f62a-103">VPN istemci paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5f62a-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="5f62a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f62a-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f62a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f62a-105">DESCRIPTION</span></span>
<span data-ttu-id="5f62a-106">**Get-AzVpnClientPackage** cmdlet 'i sanal ağ ağ GEÇIDINDEN sağlanan VPN istemci paketleriyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="5f62a-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="5f62a-107">İstemci paketleri, istemci bilgisayarın Azure sanal ağıyla VPN bağlantısı yapmasını etkinleştiren yapılandırma verilerini içerir; VPN bağlantısı oluşturmak için istemci bilgisayarlarda doğru yapılandırma paketinin yüklü olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="5f62a-108">Farklı yapılandırma paketleri, istemci bilgisayarın Windows sürümü (örneğin, Windows 7 veya Windows 10) ve istemci bilgisayarın işlemci mimarisi (AMD64 veya x86) temelinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="5f62a-109">**Get-AzVpnClientPackage** çalıştırırken mimari türünü belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="5f62a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f62a-110">EXAMPLES</span></span>

### <span data-ttu-id="5f62a-111">Örnek 1: işlemci mimarisi VPN istemci paketi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="5f62a-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="5f62a-112">Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ geçidinde depolanan AMD64 VPN istemci paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5f62a-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="5f62a-113">X86 istemci paketleri hakkında bilgi edinmek için, *ProcessorArchitecture* parametresinin değerini x86 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5f62a-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="5f62a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f62a-114">PARAMETERS</span></span>

### <span data-ttu-id="5f62a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f62a-115">-DefaultProfile</span></span>
<span data-ttu-id="5f62a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f62a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f62a-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5f62a-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="5f62a-118">İstemci paketinin tasarlandığı CPU mimarisinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="5f62a-119">Geçerli değerler amd64 ve x86 değerleridir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f62a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f62a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f62a-121">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="5f62a-122">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f62a-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5f62a-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5f62a-124">İstemci paketi bilgilerinin depolandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f62a-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f62a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f62a-125">CommonParameters</span></span>
<span data-ttu-id="5f62a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f62a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f62a-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f62a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f62a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f62a-128">INPUTS</span></span>

### <span data-ttu-id="5f62a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5f62a-129">System.String</span></span>

## <span data-ttu-id="5f62a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f62a-130">OUTPUTS</span></span>

### <span data-ttu-id="5f62a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f62a-131">System.String</span></span>

## <span data-ttu-id="5f62a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f62a-132">NOTES</span></span>

## <span data-ttu-id="5f62a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f62a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f62a-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5f62a-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5f62a-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="5f62a-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


