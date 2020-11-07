---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8171a87ea744eb708e65c71a1d25b13190b6f0fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765155"
---
# <span data-ttu-id="5f6fb-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f6fb-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5f6fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6fb-103">VPN istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f6fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f6fb-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f6fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f6fb-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6fb-106">**Get-Azurermvpnclientunkedcertificate** cmdlet 'i, sanal ağ geçidine atanan istemci iptal sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="5f6fb-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="5f6fb-108">**Get-Azurermvpnclientunkedcertificate** , tek bir sertifika hakkında bilgi almak için, ağ geçidinde tüm istemci iptal sertifikaları hakkında bilgi döndürmenizi veya *Vpnclientunkedcertificatename* parametresini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="5f6fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f6fb-109">EXAMPLES</span></span>

### <span data-ttu-id="5f6fb-110">Örnek 1: tüm istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="5f6fb-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5f6fb-111">Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ ağ geçidiyle ilişkili tüm istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="5f6fb-112">Örnek 2: belirli istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="5f6fb-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="5f6fb-113">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="5f6fb-114">Ancak, bu örnekte, döndürülen verileri belirli bir istemciye sınırlandırmak için *Vpnclientgeri* alınan bir sertifika kullanılır-iptal edildi sertifikası</span><span class="sxs-lookup"><span data-stu-id="5f6fb-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="5f6fb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f6fb-115">PARAMETERS</span></span>

### <span data-ttu-id="5f6fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="5f6fb-117">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="5f6fb-118">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="5f6fb-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5f6fb-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5f6fb-120">İptal edilen sertifika bilgilerinin atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-120">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="5f6fb-121">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="5f6fb-121">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="5f6fb-122">Bu cmdlet 'in aldığı VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-122">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f6fb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6fb-123">-DefaultProfile</span></span>
<span data-ttu-id="5f6fb-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f6fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6fb-125">CommonParameters</span></span>
<span data-ttu-id="5f6fb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6fb-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6fb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f6fb-128">INPUTS</span></span>

## <span data-ttu-id="5f6fb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f6fb-129">OUTPUTS</span></span>

###  
<span data-ttu-id="5f6fb-130">**Get-Azurermvpnclientgeri alma** **Microsoft. Azure. Commands. Network. model. psvpnclientekedcertificate** nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5f6fb-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="5f6fb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f6fb-131">NOTES</span></span>

## <span data-ttu-id="5f6fb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f6fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f6fb-133">Add-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="5f6fb-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f6fb-134">Yeni-Azurermvpnclientgeri alınamaz sertifika</span><span class="sxs-lookup"><span data-stu-id="5f6fb-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f6fb-135">Remove-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="5f6fb-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

