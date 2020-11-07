---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: a5f562fd05432abc502d648ca7fae614744e4f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939907"
---
# <span data-ttu-id="562e3-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="562e3-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="562e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="562e3-102">SYNOPSIS</span></span>
<span data-ttu-id="562e3-103">Yeni bir VPN istemcisi kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562e3-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="562e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="562e3-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="562e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="562e3-105">DESCRIPTION</span></span>
<span data-ttu-id="562e3-106">**Yeni-AzureRmVpnClientRootCertificate** cmdlet 'i sanal ağ geçidinde kullanılmak üzere yenı bir VPN kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562e3-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="562e3-107">Kök sertifikalar, kök sertifika yetkilinizi tanımlayan X. 509.440 sertifikalardır</span><span class="sxs-lookup"><span data-stu-id="562e3-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="562e3-108">Bu cmdlet, sanal ağ geçidine atanmamış tek başına bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562e3-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="562e3-109">Bunun yerine, yeni ağ geçidi oluştururken, **New-AzureRmVpnClientRootCertificate** tarafından oluşturulan sertifika New-AzureRmVirtualNetworkGateway cmdlet ile birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="562e3-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="562e3-110">Örneğin, yeni bir sertifika oluşturduğunuzu ve $Certificate adlı bir değişkende depolamanızı varsayalım.</span><span class="sxs-lookup"><span data-stu-id="562e3-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="562e3-111">Bu sertifika nesnesini, yeni sanal ağ geçidi oluştururken kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="562e3-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="562e3-112">Örneğin,</span><span class="sxs-lookup"><span data-stu-id="562e3-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="562e3-113">Daha fazla bilgi için New-AzureRmVirtualNetworkGateway cmdlet belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="562e3-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="562e3-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="562e3-114">EXAMPLES</span></span>

### <span data-ttu-id="562e3-115">Örnek 1: Aclient kök sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="562e3-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="562e3-116">Bu örnek, bir istemci kök sertifikası oluşturur ve sertifika nesnesini $Certificate adlı bir değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="562e3-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="562e3-117">Bu değişken, yeni bir sanal ağ ağ geçidine kök sertifikası eklemek için **Yeni-AzureRmVirtualNetworkGateway** cmdlet 'i tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="562e3-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="562e3-118">İlk komut **Get-Content** cmdlet 'ini kullanarak kök sertifikanın daha önce dışarı aktarılmış bir metin sunumunu alır; Bu metin verileri $Text adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="562e3-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="562e3-119">İkinci komut, ilk satır ve son satır dışında tüm metni ayıklamak için bir for döngüsü kullanır ve $CertificateText adlı bir değişkende ayıklanan metni saklar.</span><span class="sxs-lookup"><span data-stu-id="562e3-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="562e3-120">Üçüncü komut, sertifikayı oluşturmak için **New-AzureRmVpnClientRootCertificate** cmdlet 'ini kullanarak, oluşturulan nesneyi $Certificate adlı bir değişkende saklar.</span><span class="sxs-lookup"><span data-stu-id="562e3-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="562e3-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="562e3-121">PARAMETERS</span></span>

### <span data-ttu-id="562e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562e3-122">-DefaultProfile</span></span>
<span data-ttu-id="562e3-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="562e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="562e3-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="562e3-124">-Name</span></span>
<span data-ttu-id="562e3-125">Yeni istemci kök sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="562e3-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="562e3-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="562e3-126">-PublicCertData</span></span>
<span data-ttu-id="562e3-127">Eklenecek kök sertifikanın metin sunumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="562e3-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="562e3-128">Metin gösterimini almak için, sertifikanızı. cer biçiminde (base64 kodlamasını kullanarak) dışarı aktarın ve sonra sonuç dosyasını bir metin düzenleyicisinde açın.</span><span class="sxs-lookup"><span data-stu-id="562e3-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="562e3-129">Çıktıyı aşağıdakine benzer bir şekilde görmelisiniz (gerçek çıktının, burada gösterilen kısaltılmış örnekten çok daha fazla metin bulundurdığına dikkat edin):</span><span class="sxs-lookup"><span data-stu-id="562e3-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="562e3-130">---------------Son SERTIFIKA-----</span><span class="sxs-lookup"><span data-stu-id="562e3-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="562e3-131">PublicCertData, dosyadaki ilk satır (-----SERTIFIKA-----) ve son satır (-----son SERTIFIKA-----) arasındaki tüm satırlardan oluşmaktadır.</span><span class="sxs-lookup"><span data-stu-id="562e3-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="562e3-132">Aşağıdaki gibi Windows PowerShell komutlarını kullanarak PublicCertData alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="562e3-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="562e3-133">$Text = Get-Content-yol "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="562e3-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="562e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562e3-134">CommonParameters</span></span>
<span data-ttu-id="562e3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="562e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562e3-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="562e3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562e3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="562e3-137">INPUTS</span></span>

###  
<span data-ttu-id="562e3-138">Bu cmdlet, ardışık düzen girişini kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="562e3-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="562e3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="562e3-139">OUTPUTS</span></span>

###  
<span data-ttu-id="562e3-140">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate** nesnesinin yeni örneklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="562e3-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="562e3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="562e3-141">NOTES</span></span>

## <span data-ttu-id="562e3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="562e3-142">RELATED LINKS</span></span>

[<span data-ttu-id="562e3-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="562e3-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="562e3-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="562e3-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="562e3-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="562e3-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


