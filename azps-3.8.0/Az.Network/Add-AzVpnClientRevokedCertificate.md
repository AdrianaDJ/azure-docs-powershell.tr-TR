---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 54d3d5db9356badb5e9b28eeff8b51cf7b8ce504
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097999"
---
# <span data-ttu-id="c473a-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c473a-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c473a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c473a-102">SYNOPSIS</span></span>
<span data-ttu-id="c473a-103">VPN istemcisi iptal sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="c473a-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="c473a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c473a-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c473a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c473a-105">DESCRIPTION</span></span>
<span data-ttu-id="c473a-106">**Add-Azvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidine bir istemci iptal sertifikası atar.</span><span class="sxs-lookup"><span data-stu-id="c473a-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="c473a-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="c473a-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="c473a-108">Bu cmdlet 'i kullanmak için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c473a-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="c473a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c473a-109">EXAMPLES</span></span>

### <span data-ttu-id="c473a-110">Örnek 1: sanal ağ geçidine yeni bir istemci iptal sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="c473a-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c473a-111">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine yeni bir istemci iptal sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="c473a-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="c473a-112">Sertifikayı eklemek için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c473a-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="c473a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c473a-113">PARAMETERS</span></span>

### <span data-ttu-id="c473a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c473a-114">-DefaultProfile</span></span>
<span data-ttu-id="c473a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c473a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c473a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c473a-116">-ResourceGroupName</span></span>
<span data-ttu-id="c473a-117">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c473a-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="c473a-118">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="c473a-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="c473a-119">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="c473a-119">-Thumbprint</span></span>
<span data-ttu-id="c473a-120">Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c473a-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="c473a-121">Örneğin:-Parmak Izi "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Bu, aşağıdakine benzer bir Windows PowerShell komutunu kullanarak sertifikalarınız için parmak izi bilgilerini alabilirsiniz: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="c473a-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="c473a-122">Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c473a-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c473a-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c473a-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c473a-124">Sertifikanın ekleneceği sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c473a-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="c473a-125">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="c473a-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="c473a-126">Eklenecek VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c473a-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c473a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c473a-127">CommonParameters</span></span>
<span data-ttu-id="c473a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c473a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c473a-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c473a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c473a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c473a-130">INPUTS</span></span>

### <span data-ttu-id="c473a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c473a-131">System.String</span></span>

## <span data-ttu-id="c473a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c473a-132">OUTPUTS</span></span>

### <span data-ttu-id="c473a-133">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası</span><span class="sxs-lookup"><span data-stu-id="c473a-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c473a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c473a-134">NOTES</span></span>

## <span data-ttu-id="c473a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c473a-135">RELATED LINKS</span></span>

[<span data-ttu-id="c473a-136">Get-Azvpnclientgeri alma</span><span class="sxs-lookup"><span data-stu-id="c473a-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c473a-137">Yeni-Azvpnistemci geri alınamaz sertifikası</span><span class="sxs-lookup"><span data-stu-id="c473a-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c473a-138">Remove-Azvpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="c473a-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)

