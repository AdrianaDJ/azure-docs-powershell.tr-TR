---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3ea5a6ba20b02fd7289e597683d97c1513aa9873
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936588"
---
# <span data-ttu-id="a102f-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a102f-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a102f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a102f-102">SYNOPSIS</span></span>
<span data-ttu-id="a102f-103">VPN istemcisi iptal sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a102f-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="a102f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a102f-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a102f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a102f-105">DESCRIPTION</span></span>
<span data-ttu-id="a102f-106">**Remove-Azvpnclientunkedcertificate** cmdlet 'i sanal ağ ağ geçidinden bir istemci iptal sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a102f-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a102f-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="a102f-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a102f-108">İstemci tabanlı bir sertifikayı kaldırırsanız, bir sanal özel ağ (VPN) bağlantısı oluşturmak için önceden yasaklanmış sertifikayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a102f-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a102f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a102f-109">EXAMPLES</span></span>

### <span data-ttu-id="a102f-110">Örnek 1: sanal ağ ağ geçidinden istemci iptal sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="a102f-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a102f-111">Bu komut, ContosoVirtualNetwork adlı sanal ağ geçidinden bir istemci iptal sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a102f-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a102f-112">İstemci iptal sertifikasını kaldırmak için hem sertifika adını hem de sertifika parmak izini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a102f-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a102f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a102f-113">PARAMETERS</span></span>

### <span data-ttu-id="a102f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a102f-114">-DefaultProfile</span></span>
<span data-ttu-id="a102f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a102f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a102f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a102f-116">-ResourceGroupName</span></span>
<span data-ttu-id="a102f-117">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a102f-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a102f-118">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="a102f-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a102f-119">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="a102f-119">-Thumbprint</span></span>
<span data-ttu-id="a102f-120">Kaldırılmakta olan sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a102f-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="a102f-121">Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınızın parmak izi bilgilerini döndürebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a102f-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="a102f-122">Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a102f-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="a102f-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a102f-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a102f-124">Sertifikanın atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a102f-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a102f-125">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="a102f-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a102f-126">Kaldırılmakta olan VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a102f-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="a102f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a102f-127">CommonParameters</span></span>
<span data-ttu-id="a102f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a102f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a102f-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a102f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a102f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a102f-130">INPUTS</span></span>

## <span data-ttu-id="a102f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a102f-131">OUTPUTS</span></span>

## <span data-ttu-id="a102f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a102f-132">NOTES</span></span>

## <span data-ttu-id="a102f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a102f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a102f-134">Add-Azvpnistemci geri alınamaz sertifikası</span><span class="sxs-lookup"><span data-stu-id="a102f-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a102f-135">Get-Azvpnclientgeri alma</span><span class="sxs-lookup"><span data-stu-id="a102f-135">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a102f-136">Yeni-Azvpnistemci geri alınamaz sertifikası</span><span class="sxs-lookup"><span data-stu-id="a102f-136">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


