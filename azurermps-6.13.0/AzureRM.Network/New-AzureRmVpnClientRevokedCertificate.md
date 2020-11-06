---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 9f20b0540481c40326bc3656e3f65534c22f9b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589463"
---
# <span data-ttu-id="7cbdb-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7cbdb-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7cbdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbdb-103">Yeni bir VPN istemcisi iptal sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cbdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cbdb-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cbdb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cbdb-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbdb-106">**Yeni-Azurermvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidinde kullanılmak üzere yeni bir sanal özel ağ (VPN) istemci iptal sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="7cbdb-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="7cbdb-108">Bu cmdlet, sanal ağ geçidine atanmamış tek başına bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="7cbdb-109">Bunun yerine, yeni bir ağ geçidi oluştururken, **Yeni-AzurermvpnNew-AzureRmVirtualNetworkGateway clientgeri**</span><span class="sxs-lookup"><span data-stu-id="7cbdb-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="7cbdb-110">Örneğin, yeni bir sertifika oluşturduğunuzu ve $Certificate adlı bir değişkende depolamanızı varsayalım.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="7cbdb-111">Bu sertifika nesnesini, yeni sanal ağ geçidi oluştururken kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="7cbdb-112">Örneğin, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="7cbdb-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="7cbdb-113">Daha fazla bilgi için New-AzureRmVirtualNetworkGateway cmdlet belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="7cbdb-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cbdb-114">EXAMPLES</span></span>

### <span data-ttu-id="7cbdb-115">Örnek 1: yeni bir istemci oluşturma-iptal edilen sertifika</span><span class="sxs-lookup"><span data-stu-id="7cbdb-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="7cbdb-116">Bu komut yeni bir istemci-iptal edilen sertifika oluşturur ve sertifika nesnesini $Certificate adlı bir değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="7cbdb-117">Bu değişken, yeni **-AzureRmVirtualNetworkGateway** cmdlet 'i tarafından, sertifikayı yeni sanal ağ ağ geçidine eklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="7cbdb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cbdb-118">PARAMETERS</span></span>

### <span data-ttu-id="7cbdb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbdb-119">-DefaultProfile</span></span>
<span data-ttu-id="7cbdb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cbdb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7cbdb-121">-Name</span></span>
<span data-ttu-id="7cbdb-122">Yeni istemci iptal sertifikası için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="7cbdb-123">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="7cbdb-123">-Thumbprint</span></span>
<span data-ttu-id="7cbdb-124">Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="7cbdb-125">Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınızın parmak izi bilgilerini döndürebilirsiniz: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="7cbdb-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="7cbdb-126">Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="7cbdb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbdb-127">CommonParameters</span></span>
<span data-ttu-id="7cbdb-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cbdb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbdb-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cbdb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbdb-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cbdb-130">INPUTS</span></span>

### <span data-ttu-id="7cbdb-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7cbdb-131">None</span></span>

## <span data-ttu-id="7cbdb-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cbdb-132">OUTPUTS</span></span>

### <span data-ttu-id="7cbdb-133">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası</span><span class="sxs-lookup"><span data-stu-id="7cbdb-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7cbdb-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cbdb-134">NOTES</span></span>

## <span data-ttu-id="7cbdb-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cbdb-135">RELATED LINKS</span></span>

[<span data-ttu-id="7cbdb-136">Add-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="7cbdb-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7cbdb-137">Get-Azurermvpnclientgeri alma</span><span class="sxs-lookup"><span data-stu-id="7cbdb-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7cbdb-138">Remove-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="7cbdb-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


