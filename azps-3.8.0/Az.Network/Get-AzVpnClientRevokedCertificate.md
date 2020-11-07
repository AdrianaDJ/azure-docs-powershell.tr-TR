---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937673"
---
# <span data-ttu-id="e7fd1-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e7fd1-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e7fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fd1-103">VPN istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="e7fd1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7fd1-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7fd1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fd1-106">**Get-Azvpnclientunkedcertificate** cmdlet 'i, sanal ağ geçidine atanan istemci iptal sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="e7fd1-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="e7fd1-108">**Get-Azvpnclientunkedcertificate** , tek bir sertifika hakkında bilgi edinmek için ağ geçidinde tüm istemci iptal sertifikaları hakkında bilgi döndürmenizi veya *vpnclientiptal*</span><span class="sxs-lookup"><span data-stu-id="e7fd1-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="e7fd1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7fd1-109">EXAMPLES</span></span>

### <span data-ttu-id="e7fd1-110">Örnek 1: tüm istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="e7fd1-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e7fd1-111">Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ ağ geçidiyle ilişkili tüm istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="e7fd1-112">Örnek 2: belirli istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="e7fd1-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="e7fd1-113">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="e7fd1-114">Ancak, bu örnekte, döndürülen verileri belirli bir istemciye sınırlandırmak için *Vpnclientgeri* alınan bir sertifika kullanılır-iptal edildi sertifikası</span><span class="sxs-lookup"><span data-stu-id="e7fd1-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="e7fd1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7fd1-115">PARAMETERS</span></span>

### <span data-ttu-id="e7fd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fd1-116">-DefaultProfile</span></span>
<span data-ttu-id="e7fd1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7fd1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fd1-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7fd1-119">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="e7fd1-120">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="e7fd1-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e7fd1-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e7fd1-122">İptal edilen sertifika bilgilerinin atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="e7fd1-123">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="e7fd1-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="e7fd1-124">Bu cmdlet 'in aldığı VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e7fd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fd1-125">CommonParameters</span></span>
<span data-ttu-id="e7fd1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fd1-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fd1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7fd1-128">INPUTS</span></span>

### <span data-ttu-id="e7fd1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e7fd1-129">System.String</span></span>

## <span data-ttu-id="e7fd1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7fd1-130">OUTPUTS</span></span>

### <span data-ttu-id="e7fd1-131">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası</span><span class="sxs-lookup"><span data-stu-id="e7fd1-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e7fd1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7fd1-132">NOTES</span></span>

## <span data-ttu-id="e7fd1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7fd1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7fd1-134">Add-Azvpnistemci geri alınamaz sertifikası</span><span class="sxs-lookup"><span data-stu-id="e7fd1-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e7fd1-135">Yeni-Azvpnistemci geri alınamaz sertifikası</span><span class="sxs-lookup"><span data-stu-id="e7fd1-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e7fd1-136">Remove-Azvpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="e7fd1-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


