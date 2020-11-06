---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 95442c724548119726aa466edf1b4fa223271865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594362"
---
# <span data-ttu-id="5e776-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e776-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="5e776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e776-102">SYNOPSIS</span></span>
<span data-ttu-id="5e776-103">Mevcut bir VPN istemcisi kök sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e776-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e776-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e776-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e776-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e776-105">DESCRIPTION</span></span>
<span data-ttu-id="5e776-106">**Remove-AzureRmVpnClientRootCertificate** cmdlet 'i, belirtilen kök sertifikayı sanal ağ ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e776-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="5e776-107">Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır</span><span class="sxs-lookup"><span data-stu-id="5e776-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="5e776-108">Kimlik doğrulama amacıyla sertifikayı kullanan bir kök sertifikayı kaldırırsanız, artık ağ geçidine bağlanamaz.</span><span class="sxs-lookup"><span data-stu-id="5e776-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="5e776-109">**Remove-AzureRmVpnClientRootCertificate** kullandığınızda, sertifika verilerinin hem sertifika adını hem de metin gösterimini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5e776-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="5e776-110">Sertifikanın metin gösterimi hakkında daha fazla bilgi için, *Publiccertdata* parametre açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="5e776-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="5e776-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e776-111">EXAMPLES</span></span>

### <span data-ttu-id="5e776-112">Örnek 1: sanal ağ ağ geçidinden istemci kök sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e776-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="5e776-113">Bu örnekte, ContosoRootCertificate adlı bir istemci kök sertifikası sanal ağ geçidinden ContosoVirtualGateway 'den kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="5e776-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="5e776-114">İlk komut, sertifikanın önceden dışarı aktarılmış bir metin sunumunu almak için **Get-Content** cmdlet 'ini kullanır; Bu metin gösterimi $Text adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="5e776-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="5e776-115">İkinci komut, ilk satır ve son satır dışında $Text tüm metni ayıklamak için bir for döngüsü kullanır.</span><span class="sxs-lookup"><span data-stu-id="5e776-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="5e776-116">Bu ayıklanan metin $CertificateText adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="5e776-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="5e776-117">Üçüncü komut, **Remove-AzureRmVpnClientRootCertificate** cmdlet 'ini kullanarak sertifikayı ağ geçidinden kaldırmak için $CertificateText değişkeninde depolanan bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="5e776-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="5e776-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e776-118">PARAMETERS</span></span>

### <span data-ttu-id="5e776-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e776-119">-DefaultProfile</span></span>
<span data-ttu-id="5e776-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e776-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e776-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="5e776-121">-PublicCertData</span></span>
<span data-ttu-id="5e776-122">Kaldırılacak kök sertifikanın metin gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e776-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="5e776-123">Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="5e776-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="5e776-124">Aşağıdakine benzer bir çıkışı görmeniz gerekir (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin içerdiğine dikkat edin):---------------son SERTIFIKAYı-----PublicCertData ilk satır (----------SERTIFIKA-----) ve son satır (-----son SERTIFIKA) arasındaki tüm satırlardan oluşmuştur.</span><span class="sxs-lookup"><span data-stu-id="5e776-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="5e776-125">PublicCertData 'ı, buna benzer Windows PowerShell komutlarını kullanarak da alabilirsiniz: $Text = Get-Content-yol "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = $i for = 1; $i-a $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="5e776-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="5e776-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e776-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e776-127">Sanal ağ geçidinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e776-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="5e776-128">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="5e776-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="5e776-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5e776-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5e776-130">Sertifikanın kaldırıldığı sanal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e776-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="5e776-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="5e776-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="5e776-132">Bu cmdlet 'in kaldırıldığı istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e776-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e776-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e776-133">CommonParameters</span></span>
<span data-ttu-id="5e776-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e776-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e776-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e776-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e776-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e776-136">INPUTS</span></span>

### <span data-ttu-id="5e776-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5e776-137">System.String</span></span>

## <span data-ttu-id="5e776-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e776-138">OUTPUTS</span></span>

### <span data-ttu-id="5e776-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e776-139">System.Boolean</span></span>

## <span data-ttu-id="5e776-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e776-140">NOTES</span></span>

## <span data-ttu-id="5e776-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e776-141">RELATED LINKS</span></span>

[<span data-ttu-id="5e776-142">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e776-142">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="5e776-143">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5e776-143">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="5e776-144">Yeni-Azurermvpnclientrootsertifikası</span><span class="sxs-lookup"><span data-stu-id="5e776-144">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


