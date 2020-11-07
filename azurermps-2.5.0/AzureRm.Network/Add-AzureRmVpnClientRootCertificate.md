---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 2f5d73cd06d975d6458776dee4242b392b5c160b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940109"
---
# <span data-ttu-id="cd198-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd198-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="cd198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd198-102">SYNOPSIS</span></span>
<span data-ttu-id="cd198-103">VPN istemcisi kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cd198-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd198-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd198-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd198-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd198-105">DESCRIPTION</span></span>
<span data-ttu-id="cd198-106">**Add-AzureRmVpnClientRootCertificate** cmdlet 'i sanal ağ geçidine kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cd198-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="cd198-107">Kök sertifikalar, kök sertifika yetkilinize tanımlayan X. 509.440 sertifikalardır.</span><span class="sxs-lookup"><span data-stu-id="cd198-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="cd198-108">Tasarım olarak, ağ geçidinde kullanılan tüm sertifikalar kök sertifikaya güvenir.</span><span class="sxs-lookup"><span data-stu-id="cd198-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="cd198-109">Bu cmdlet, var olan bir sertifikayı ağ geçidi kök sertifikası olarak atar.</span><span class="sxs-lookup"><span data-stu-id="cd198-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="cd198-110">Bir X. 509.440 sertifikanız yoksa, ortak anahtar altyapınız üzerinden bir tane oluşturabilir veya makecert.exe gibi bir sertifika Oluşturucusu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd198-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="cd198-111">Kök sertifika eklemek için, sertifika adını belirtmeniz ve sertifikanın salt metin bir gösterimini sağlamanız gerekir (daha fazla bilgi için *PublicCertData* parametresine bakın).</span><span class="sxs-lookup"><span data-stu-id="cd198-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="cd198-112">Azure, bir ağ geçidine birden fazla kök sertifikası atamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="cd198-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="cd198-113">Birden çok kök sertifika genellikle birden fazla şirketten Kullanıcı içeren kuruluşlar tarafından dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="cd198-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="cd198-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd198-114">EXAMPLES</span></span>

### <span data-ttu-id="cd198-115">Örnek 1: sanal ağ geçidine istemci kök sertifikası ekleme</span><span class="sxs-lookup"><span data-stu-id="cd198-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="cd198-116">Bu örnek, ContosoVirtualGateway adlı sanal bir ağ geçidine bir istemci kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cd198-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="cd198-117">İlk komut **Get-Content** cmdlet 'ini kullanarak kök sertifikanın önceden dışarı aktarılmış bir metin sunumunu alır ve bu metin verilerinin $Text adlı değişkeni depolar.</span><span class="sxs-lookup"><span data-stu-id="cd198-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="cd198-118">İkinci komut, ilk satır ve son satır dışında tüm metni ayıklamak için bir for döngüsü kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd198-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="cd198-119">Ayıklanan metin $CertificateText adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="cd198-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="cd198-120">Üçüncü komut, kök sertifikayı ağ geçidine eklemek için **Add-AzureRmVpnClientRootCertificate** cmdlet 'i ile $CertificateText 'de depolanan metni kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd198-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="cd198-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd198-121">PARAMETERS</span></span>

### <span data-ttu-id="cd198-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd198-122">-DefaultProfile</span></span>
<span data-ttu-id="cd198-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd198-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd198-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="cd198-124">-PublicCertData</span></span>
<span data-ttu-id="cd198-125">Eklenecek kök sertifikanın metin gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd198-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="cd198-126">Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kodlamasını kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="cd198-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="cd198-127">Bunu yaptığınızda, çıktıyı aşağıdakine benzer şekilde görürsünüz (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin satırı içereceği unutmayın):</span><span class="sxs-lookup"><span data-stu-id="cd198-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="cd198-128">---------------Son SERTIFIKA-----</span><span class="sxs-lookup"><span data-stu-id="cd198-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="cd198-129">PublicCertData, dosyadaki ilk satır (-----SERTIFIKA-----) ve son satır (-----son SERTIFIKA-----) arasındaki tüm satırlardan oluşmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cd198-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="cd198-130">Bu verileri, aşağıdakine benzer Windows PowerShell komutlarını kullanarak alabilirsiniz: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="cd198-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="cd198-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd198-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd198-132">Kök sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd198-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="cd198-133">Kaynak grupları, stok yönetimini ve genel Azure yönetimini basitleştirmeye yardımcı olmak için öğeleri kategorilere ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="cd198-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="cd198-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cd198-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cd198-135">Sertifikanın eklendiği sanal ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd198-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="cd198-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="cd198-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="cd198-137">Bu cmdlet 'in eklediği istemci kök sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd198-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cd198-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd198-138">CommonParameters</span></span>
<span data-ttu-id="cd198-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd198-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd198-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd198-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd198-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd198-141">INPUTS</span></span>

## <span data-ttu-id="cd198-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd198-142">OUTPUTS</span></span>

### <span data-ttu-id="cd198-143">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd198-143">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="cd198-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd198-144">NOTES</span></span>

## <span data-ttu-id="cd198-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd198-145">RELATED LINKS</span></span>

[<span data-ttu-id="cd198-146">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd198-146">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="cd198-147">Yeni-Azurermvpnclientrootsertifikası</span><span class="sxs-lookup"><span data-stu-id="cd198-147">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="cd198-148">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd198-148">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


