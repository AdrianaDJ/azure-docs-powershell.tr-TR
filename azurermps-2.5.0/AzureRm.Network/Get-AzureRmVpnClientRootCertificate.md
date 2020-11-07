---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939309"
---
# <span data-ttu-id="ae854-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae854-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="ae854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae854-102">SYNOPSIS</span></span>
<span data-ttu-id="ae854-103">VPN kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ae854-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae854-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae854-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae854-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae854-105">DESCRIPTION</span></span>
<span data-ttu-id="ae854-106">**Get-AzureRmVpnClientRootCertificate** cmdlet 'i, sanal ağ geçidine atanan kök sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae854-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="ae854-107">Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır</span><span class="sxs-lookup"><span data-stu-id="ae854-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="ae854-108">**Get-AzureRmVpnClientRootCertificate** , varsayılan olarak ağ geçidine atanmış olan tüm kök sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae854-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="ae854-109">(Ağ geçitleri birden fazla kök sertifikaya sahip olabilir.) Ancak, **Vpnclientrootcertificatename** parametresini ekleyerek, döndürülen verileri belirli bir sertifikayla sınırlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae854-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="ae854-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae854-110">EXAMPLES</span></span>

### <span data-ttu-id="ae854-111">Örnek 1: tüm kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="ae854-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="ae854-112">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine atanan tüm kök sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ae854-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="ae854-113">Örnek 2: belirli kök sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="ae854-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="ae854-114">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="ae854-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="ae854-115">Bu durumda, döndürülen verileri belirli bir kök sertifikaya sınırlandırmak için *Vpnclientrootcertificatename* parametresi eklenmiştir: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="ae854-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="ae854-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae854-116">PARAMETERS</span></span>

### <span data-ttu-id="ae854-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae854-117">-DefaultProfile</span></span>
<span data-ttu-id="ae854-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae854-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae854-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae854-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae854-120">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae854-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="ae854-121">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="ae854-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae854-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ae854-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ae854-123">Kök sertifikanın atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae854-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae854-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="ae854-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="ae854-125">Bu cmdlet 'in aldığı istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae854-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae854-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae854-126">CommonParameters</span></span>
<span data-ttu-id="ae854-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae854-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae854-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae854-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae854-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae854-129">INPUTS</span></span>

## <span data-ttu-id="ae854-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae854-130">OUTPUTS</span></span>

###  
<span data-ttu-id="ae854-131">**Get-AzureRmVpnClientRootCertificate** , **Microsoft. Azure. Commands. Network. model. psvpnclientrootcertificate** nesnesinin örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ae854-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="ae854-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae854-132">NOTES</span></span>

## <span data-ttu-id="ae854-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae854-133">RELATED LINKS</span></span>

[<span data-ttu-id="ae854-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae854-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="ae854-135">Yeni-Azurermvpnclientrootsertifikası</span><span class="sxs-lookup"><span data-stu-id="ae854-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="ae854-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae854-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


