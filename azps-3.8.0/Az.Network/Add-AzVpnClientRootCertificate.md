---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097996"
---
# <span data-ttu-id="1db9c-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db9c-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="1db9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1db9c-103">VPN istemcisi kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="1db9c-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="1db9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1db9c-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1db9c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db9c-105">DESCRIPTION</span></span>
<span data-ttu-id="1db9c-106">**Add-AzVpnClientRootCertificate** cmdlet 'i sanal ağ geçidine kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="1db9c-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="1db9c-107">Kök sertifikalar, kök sertifika yetkilinize tanımlayan X. 509.440 sertifikalardır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="1db9c-108">Tasarım olarak, ağ geçidinde kullanılan tüm sertifikalar kök sertifikaya güvenir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="1db9c-109">Bu cmdlet, var olan bir sertifikayı ağ geçidi kök sertifikası olarak atar.</span><span class="sxs-lookup"><span data-stu-id="1db9c-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="1db9c-110">Bir X. 509.440 sertifikanız yoksa, ortak anahtar altyapınız üzerinden bir tane oluşturabilir veya makecert.exe gibi bir sertifika Oluşturucusu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db9c-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="1db9c-111">Kök sertifika eklemek için, sertifika adını belirtmeniz ve sertifikanın salt metin bir gösterimini sağlamanız gerekir (daha fazla bilgi için *PublicCertData* parametresine bakın).</span><span class="sxs-lookup"><span data-stu-id="1db9c-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="1db9c-112">Azure, bir ağ geçidine birden fazla kök sertifikası atamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="1db9c-113">Birden çok kök sertifika genellikle birden fazla şirketten Kullanıcı içeren kuruluşlar tarafından dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="1db9c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1db9c-114">EXAMPLES</span></span>

### <span data-ttu-id="1db9c-115">Örnek 1: sanal ağ geçidine istemci kök sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="1db9c-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="1db9c-116">Bu örnek, ContosoVirtualGateway adlı sanal bir ağ geçidine bir istemci kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="1db9c-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="1db9c-117">İlk komut **Get-Content** cmdlet 'ini kullanarak kök sertifikanın önceden dışarı aktarılmış bir metin sunumunu alır ve bu metin verilerinin $Text adlı değişkeni depolar.</span><span class="sxs-lookup"><span data-stu-id="1db9c-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="1db9c-118">İkinci komut, ilk satır ve son satır dışında tüm metni ayıklamak için bir for döngüsü kullanır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="1db9c-119">Ayıklanan metin $CertificateText adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="1db9c-120">Üçüncü komut, kök sertifikayı ağ geçidine eklemek için **Add-AzVpnClientRootCertificate** cmdlet 'i ile $CertificateText depolanan metni kullanır.</span><span class="sxs-lookup"><span data-stu-id="1db9c-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="1db9c-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1db9c-121">PARAMETERS</span></span>

### <span data-ttu-id="1db9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db9c-122">-DefaultProfile</span></span>
<span data-ttu-id="1db9c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1db9c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1db9c-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="1db9c-124">-PublicCertData</span></span>
<span data-ttu-id="1db9c-125">Eklenecek kök sertifikanın metin gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="1db9c-126">Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kodlamasını kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="1db9c-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="1db9c-127">Bunu yaptığınızda, aşağıdakine benzer bir çıkış görürsünüz (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin içerdiğine dikkat edin):---------------son SERTIFIKA-----, PublicCertData ilk satır (----------SERTIFIKA-----) ve son satır (-----son SERTIFIKA) arasındaki tüm satırlardan oluşmuştur.</span><span class="sxs-lookup"><span data-stu-id="1db9c-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="1db9c-128">Bu verileri, aşağıdakine benzer Windows PowerShell komutlarını kullanarak alabilirsiniz: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="1db9c-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="1db9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="1db9c-130">Kök sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="1db9c-131">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1db9c-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1db9c-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1db9c-133">Sertifikanın eklendiği sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="1db9c-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="1db9c-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="1db9c-135">Bu cmdlet 'in eklediği istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1db9c-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1db9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db9c-136">CommonParameters</span></span>
<span data-ttu-id="1db9c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1db9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db9c-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1db9c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db9c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1db9c-139">INPUTS</span></span>

### <span data-ttu-id="1db9c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1db9c-140">System.String</span></span>

## <span data-ttu-id="1db9c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1db9c-141">OUTPUTS</span></span>

### <span data-ttu-id="1db9c-142">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db9c-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="1db9c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1db9c-143">NOTES</span></span>

## <span data-ttu-id="1db9c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1db9c-144">RELATED LINKS</span></span>

[<span data-ttu-id="1db9c-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db9c-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="1db9c-146">Yeni-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db9c-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="1db9c-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db9c-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

