---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 6303aeac769b2303e8ebbd67a237d2eaf99ed9cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589479"
---
# <span data-ttu-id="02c73-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="02c73-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="02c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c73-102">SYNOPSIS</span></span>
<span data-ttu-id="02c73-103">VPN kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="02c73-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02c73-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02c73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02c73-105">DESCRIPTION</span></span>
<span data-ttu-id="02c73-106">**Get-AzureRmVpnClientRootCertificate** cmdlet 'i, sanal ağ geçidine atanan kök sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="02c73-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="02c73-107">Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır</span><span class="sxs-lookup"><span data-stu-id="02c73-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="02c73-108">**Get-AzureRmVpnClientRootCertificate** , varsayılan olarak ağ geçidine atanmış olan tüm kök sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="02c73-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="02c73-109">(Ağ geçitleri birden fazla kök sertifikaya sahip olabilir.) Ancak, **Vpnclientrootcertificatename** parametresini ekleyerek, döndürülen verileri belirli bir sertifikayla sınırlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02c73-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="02c73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02c73-110">EXAMPLES</span></span>

### <span data-ttu-id="02c73-111">Örnek 1: tüm kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="02c73-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="02c73-112">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine atanan tüm kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="02c73-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="02c73-113">Örnek 2: belirli kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="02c73-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="02c73-114">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="02c73-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="02c73-115">Bu durumda, döndürülen verileri belirli bir kök sertifikaya sınırlandırmak için *Vpnclientrootcertificatename* parametresi eklenmiştir: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="02c73-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="02c73-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02c73-116">PARAMETERS</span></span>

### <span data-ttu-id="02c73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c73-117">-DefaultProfile</span></span>
<span data-ttu-id="02c73-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02c73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c73-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c73-119">-ResourceGroupName</span></span>
<span data-ttu-id="02c73-120">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02c73-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="02c73-121">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="02c73-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c73-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="02c73-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="02c73-123">Kök sertifikanın atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02c73-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c73-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="02c73-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="02c73-125">Bu cmdlet 'in aldığı istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02c73-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c73-126">CommonParameters</span></span>
<span data-ttu-id="02c73-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02c73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c73-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c73-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c73-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02c73-129">INPUTS</span></span>

### <span data-ttu-id="02c73-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02c73-130">System.String</span></span>

## <span data-ttu-id="02c73-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02c73-131">OUTPUTS</span></span>

### <span data-ttu-id="02c73-132">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="02c73-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="02c73-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02c73-133">NOTES</span></span>

## <span data-ttu-id="02c73-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02c73-134">RELATED LINKS</span></span>

[<span data-ttu-id="02c73-135">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="02c73-135">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="02c73-136">Yeni-Azurermvpnclientrootsertifikası</span><span class="sxs-lookup"><span data-stu-id="02c73-136">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="02c73-137">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="02c73-137">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


