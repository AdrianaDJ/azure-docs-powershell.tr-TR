---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: e9095c5f2e8f2a9820214f1144f10f8049f22027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588455"
---
# <span data-ttu-id="a316e-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a316e-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a316e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a316e-102">SYNOPSIS</span></span>
<span data-ttu-id="a316e-103">VPN istemcisi iptal sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a316e-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a316e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a316e-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a316e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a316e-105">DESCRIPTION</span></span>
<span data-ttu-id="a316e-106">**Remove-Azurermvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidinden bir istemci iptal sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a316e-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a316e-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="a316e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a316e-108">İstemci tabanlı bir sertifikayı kaldırırsanız, bir sanal özel ağ (VPN) bağlantısı oluşturmak için önceden yasaklanmış sertifikayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a316e-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a316e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a316e-109">EXAMPLES</span></span>

### <span data-ttu-id="a316e-110">Örnek 1: sanal ağ ağ geçidinden istemci iptal sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="a316e-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a316e-111">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidinden bir istemci iptal sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a316e-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a316e-112">İstemci iptal sertifikasını kaldırmak için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a316e-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a316e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a316e-113">PARAMETERS</span></span>

### <span data-ttu-id="a316e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a316e-114">-DefaultProfile</span></span>
<span data-ttu-id="a316e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a316e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a316e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a316e-116">-ResourceGroupName</span></span>
<span data-ttu-id="a316e-117">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a316e-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a316e-118">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="a316e-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a316e-119">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="a316e-119">-Thumbprint</span></span>
<span data-ttu-id="a316e-120">Kaldırılmakta olan sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a316e-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="a316e-121">Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınızın parmak izi bilgilerini döndürebilirsiniz: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="a316e-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="a316e-122">Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a316e-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="a316e-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a316e-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a316e-124">Sertifikanın atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a316e-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a316e-125">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="a316e-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a316e-126">Kaldırılmakta olan VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a316e-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="a316e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a316e-127">CommonParameters</span></span>
<span data-ttu-id="a316e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a316e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a316e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a316e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a316e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a316e-130">INPUTS</span></span>

### <span data-ttu-id="a316e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a316e-131">System.String</span></span>

## <span data-ttu-id="a316e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a316e-132">OUTPUTS</span></span>

### <span data-ttu-id="a316e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a316e-133">System.Boolean</span></span>

## <span data-ttu-id="a316e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a316e-134">NOTES</span></span>

## <span data-ttu-id="a316e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a316e-135">RELATED LINKS</span></span>

[<span data-ttu-id="a316e-136">Add-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="a316e-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a316e-137">Get-Azurermvpnclientgeri alma</span><span class="sxs-lookup"><span data-stu-id="a316e-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a316e-138">Yeni-Azurermvpnclientgeri alınamaz sertifika</span><span class="sxs-lookup"><span data-stu-id="a316e-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


