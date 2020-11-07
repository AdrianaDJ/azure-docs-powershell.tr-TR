---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: 1a75338b7c2b83f505c82ebc714ea583b3162eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763261"
---
# <span data-ttu-id="8e3a8-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="8e3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3a8-103">VPN istemci paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e3a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e3a8-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3a8-106">**Get-AzureRmVpnClientPackage** cmdlet 'i sanal ağ ağ GEÇIDINDEN sağlanan VPN istemci paketleriyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="8e3a8-107">İstemci paketleri, istemci bilgisayarın Azure sanal ağıyla VPN bağlantısı yapmasını etkinleştiren yapılandırma verilerini içerir; VPN bağlantısı oluşturmak için istemci bilgisayarlarda doğru yapılandırma paketinin yüklü olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="8e3a8-108">Farklı yapılandırma paketleri, istemci bilgisayarın Windows sürümü (örneğin, Windows 7 veya Windows 10) ve istemci bilgisayarın işlemci mimarisi (AMD64 veya x86) temelinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="8e3a8-109">**Get-AzureRmVpnClientPackage** çalıştırırken mimari türünü belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="8e3a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e3a8-110">EXAMPLES</span></span>

### <span data-ttu-id="8e3a8-111">Örnek 1: işlemci mimarisi VPN istemci paketi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="8e3a8-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="8e3a8-112">Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ geçidinde depolanan AMD64 VPN istemci paketi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="8e3a8-113">X86 istemci paketleri hakkında bilgi edinmek için, *ProcessorArchitecture* parametresinin değerini x86 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="8e3a8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e3a8-114">PARAMETERS</span></span>

### <span data-ttu-id="8e3a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-115">-DefaultProfile</span></span>
<span data-ttu-id="8e3a8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e3a8-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8e3a8-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="8e3a8-118">İstemci paketinin tasarlandığı CPU mimarisinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="8e3a8-119">Geçerli değerler amd64 ve x86 değerleridir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e3a8-121">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="8e3a8-122">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3a8-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e3a8-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8e3a8-124">İstemci paketi bilgilerinin depolandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3a8-125">CommonParameters</span></span>
<span data-ttu-id="8e3a8-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3a8-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3a8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3a8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e3a8-128">INPUTS</span></span>

### <span data-ttu-id="8e3a8-129">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8e3a8-129">String</span></span>
<span data-ttu-id="8e3a8-130">' ResourceGroupName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e3a8-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8e3a8-131">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8e3a8-131">String</span></span>
<span data-ttu-id="8e3a8-132">' VirtualNetworkGatewayName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8e3a8-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8e3a8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e3a8-133">OUTPUTS</span></span>

###  
<span data-ttu-id="8e3a8-134">**Get-AzureRmVpnClientPackage** , System. String nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e3a8-134">**Get-AzureRmVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="8e3a8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e3a8-135">NOTES</span></span>

## <span data-ttu-id="8e3a8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e3a8-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e3a8-137">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8e3a8-137">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8e3a8-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


