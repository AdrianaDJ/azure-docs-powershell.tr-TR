---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940110"
---
# <span data-ttu-id="0253c-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0253c-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="0253c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0253c-102">SYNOPSIS</span></span>
<span data-ttu-id="0253c-103">VPN istemcisi iptal sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="0253c-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0253c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0253c-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0253c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0253c-105">DESCRIPTION</span></span>
<span data-ttu-id="0253c-106">**Add-Azurermvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidine bir istemci iptal sertifikası atar.</span><span class="sxs-lookup"><span data-stu-id="0253c-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="0253c-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="0253c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="0253c-108">Bu cmdlet 'i kullanmak için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0253c-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="0253c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0253c-109">EXAMPLES</span></span>

### <span data-ttu-id="0253c-110">Örnek 1: sanal ağ geçidine yeni bir istemci iptal sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="0253c-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="0253c-111">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidine yeni bir istemci iptal sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="0253c-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="0253c-112">Sertifikayı eklemek için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0253c-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="0253c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0253c-113">PARAMETERS</span></span>

### <span data-ttu-id="0253c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0253c-114">-DefaultProfile</span></span>
<span data-ttu-id="0253c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0253c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0253c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0253c-116">-ResourceGroupName</span></span>
<span data-ttu-id="0253c-117">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0253c-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="0253c-118">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="0253c-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="0253c-119">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="0253c-119">-Thumbprint</span></span>
<span data-ttu-id="0253c-120">Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0253c-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="0253c-121">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0253c-121">For example:</span></span>

<span data-ttu-id="0253c-122">-Parmak izi "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="0253c-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="0253c-123">Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınız için parmak izi bilgilerini alabilirsiniz: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="0253c-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="0253c-124">Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0253c-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0253c-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0253c-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0253c-126">Sertifikanın ekleneceği sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0253c-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="0253c-127">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="0253c-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="0253c-128">Eklenecek VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0253c-128">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0253c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0253c-129">CommonParameters</span></span>
<span data-ttu-id="0253c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0253c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0253c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0253c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0253c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0253c-132">INPUTS</span></span>

## <span data-ttu-id="0253c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0253c-133">OUTPUTS</span></span>

### <span data-ttu-id="0253c-134">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası</span><span class="sxs-lookup"><span data-stu-id="0253c-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="0253c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0253c-135">NOTES</span></span>

## <span data-ttu-id="0253c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0253c-136">RELATED LINKS</span></span>

[<span data-ttu-id="0253c-137">Get-Azurermvpnclientgeri alma</span><span class="sxs-lookup"><span data-stu-id="0253c-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="0253c-138">Yeni-Azurermvpnclientgeri alınamaz sertifika</span><span class="sxs-lookup"><span data-stu-id="0253c-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="0253c-139">Remove-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="0253c-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


