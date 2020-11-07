---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 847f1c06975e9bef570c5ab3fdaf5f6f3e4a99d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918383"
---
# <span data-ttu-id="74046-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="74046-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="74046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74046-102">SYNOPSIS</span></span>
<span data-ttu-id="74046-103">VPN kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="74046-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="74046-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74046-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74046-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74046-105">DESCRIPTION</span></span>
<span data-ttu-id="74046-106">**Get-AzVpnClientRootCertificate** cmdlet 'i, sanal ağ geçidine atanan kök sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="74046-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="74046-107">Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır</span><span class="sxs-lookup"><span data-stu-id="74046-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="74046-108">Varsayılan olarak **Get-AzVpnClientRootCertificate** , bir ağ geçidine atanmış olan tüm kök sertifikaları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="74046-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="74046-109">(Ağ geçitleri birden fazla kök sertifikaya sahip olabilir.) Ancak, **Vpnclientrootcertificatename** parametresini ekleyerek, döndürülen verileri belirli bir sertifikayla sınırlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74046-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="74046-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74046-110">EXAMPLES</span></span>

### <span data-ttu-id="74046-111">Örnek 1: tüm kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="74046-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="74046-112">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine atanan tüm kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="74046-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="74046-113">Örnek 2: belirli kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="74046-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="74046-114">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="74046-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="74046-115">Bu durumda, döndürülen verileri belirli bir kök sertifikaya sınırlandırmak için *Vpnclientrootcertificatename* parametresi eklenmiştir: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="74046-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="74046-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74046-116">PARAMETERS</span></span>

### <span data-ttu-id="74046-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74046-117">-DefaultProfile</span></span>
<span data-ttu-id="74046-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74046-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74046-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74046-119">-ResourceGroupName</span></span>
<span data-ttu-id="74046-120">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74046-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="74046-121">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="74046-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="74046-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="74046-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="74046-123">Kök sertifikanın atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74046-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="74046-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="74046-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="74046-125">Bu cmdlet 'in aldığı istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74046-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="74046-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74046-126">CommonParameters</span></span>
<span data-ttu-id="74046-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74046-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74046-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74046-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74046-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74046-129">INPUTS</span></span>

### <span data-ttu-id="74046-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74046-130">System.String</span></span>

## <span data-ttu-id="74046-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74046-131">OUTPUTS</span></span>

### <span data-ttu-id="74046-132">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="74046-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="74046-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74046-133">NOTES</span></span>

## <span data-ttu-id="74046-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74046-134">RELATED LINKS</span></span>

[<span data-ttu-id="74046-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="74046-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="74046-136">Yeni-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="74046-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="74046-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="74046-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


