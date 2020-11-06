---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 2bbfaa264a772f821ee22ef0a7b218f70700343c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590409"
---
# <span data-ttu-id="3d925-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3d925-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="3d925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d925-102">SYNOPSIS</span></span>
<span data-ttu-id="3d925-103">VPN istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3d925-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d925-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d925-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d925-105">DESCRIPTION</span></span>
<span data-ttu-id="3d925-106">**Get-Azurermvpnclientunkedcertificate** cmdlet 'i, sanal ağ geçidine atanan istemci iptal sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="3d925-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="3d925-107">İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.</span><span class="sxs-lookup"><span data-stu-id="3d925-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="3d925-108">**Get-Azurermvpnclientunkedcertificate** , tek bir sertifika hakkında bilgi almak için, ağ geçidinde tüm istemci iptal sertifikaları hakkında bilgi döndürmenizi veya *Vpnclientunkedcertificatename* parametresini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="3d925-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="3d925-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d925-109">EXAMPLES</span></span>

### <span data-ttu-id="3d925-110">Örnek 1: tüm istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="3d925-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="3d925-111">Bu komut, ContosoVirtualNetworkGateway adındaki sanal ağ ağ geçidiyle ilişkili tüm istemci iptal sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3d925-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="3d925-112">Örnek 2: belirli istemci iptal sertifikaları hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="3d925-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="3d925-113">Bu komut, örnek 1 ' de gösterilen komutun bir çeşitlemesi.</span><span class="sxs-lookup"><span data-stu-id="3d925-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="3d925-114">Ancak, bu örnekte, döndürülen verileri belirli bir istemciye sınırlandırmak için *Vpnclientgeri* alınan bir sertifika kullanılır-iptal edildi sertifikası</span><span class="sxs-lookup"><span data-stu-id="3d925-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="3d925-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d925-115">PARAMETERS</span></span>

### <span data-ttu-id="3d925-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d925-116">-DefaultProfile</span></span>
<span data-ttu-id="3d925-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d925-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d925-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d925-118">-ResourceGroupName</span></span>
<span data-ttu-id="3d925-119">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d925-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="3d925-120">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="3d925-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3d925-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3d925-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3d925-122">İptal edilen sertifika bilgilerinin atandığı sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d925-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="3d925-123">-Vpnclientiptal</span><span class="sxs-lookup"><span data-stu-id="3d925-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="3d925-124">Bu cmdlet 'in aldığı VPN istemci sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d925-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3d925-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d925-125">CommonParameters</span></span>
<span data-ttu-id="3d925-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d925-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d925-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d925-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d925-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d925-128">INPUTS</span></span>

### <span data-ttu-id="3d925-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3d925-129">None</span></span>
<span data-ttu-id="3d925-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3d925-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d925-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d925-131">OUTPUTS</span></span>

###  
<span data-ttu-id="3d925-132">**Get-Azurermvpnclientgeri alma** **Microsoft. Azure. Commands. Network. model. psvpnclientekedcertificate** nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3d925-132">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="3d925-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d925-133">NOTES</span></span>

## <span data-ttu-id="3d925-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d925-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d925-135">Add-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="3d925-135">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="3d925-136">Yeni-Azurermvpnclientgeri alınamaz sertifika</span><span class="sxs-lookup"><span data-stu-id="3d925-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="3d925-137">Remove-Azurermvpnclientekedcertificate</span><span class="sxs-lookup"><span data-stu-id="3d925-137">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


