---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 517614e93510aab163f5d632705e4a5a3566186a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589881"
---
# <span data-ttu-id="00b09-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="00b09-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="00b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b09-102">SYNOPSIS</span></span>
<span data-ttu-id="00b09-103">Bir sanal makineye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="00b09-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00b09-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [<CommonParameters>]
```

## <span data-ttu-id="00b09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00b09-105">DESCRIPTION</span></span>
<span data-ttu-id="00b09-106">**Add-AzureRmVMSecret** cmdlet 'i bir sanal makineye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="00b09-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="00b09-107">Bu değer, sanal makineye sertifika eklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="00b09-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="00b09-108">Gizli anahtar bir kasaya depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="00b09-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="00b09-109">Anahtar Kasası hakkında daha fazla bilgi için [Azure Anahtar Kasası nedir?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="00b09-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="00b09-110">Cmdlet 'ler hakkında daha fazla bilgi için, Microsoft Geliştirici ağ kitaplığında veya [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet 'Inde [Azure Key kasa cmdlet 'lerini](https://msdn.microsoft.com/library/azure/dn868052.aspx) görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00b09-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="00b09-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00b09-111">EXAMPLES</span></span>

### <span data-ttu-id="00b09-112">Örnek 1: sanal makineye parola ekleme</span><span class="sxs-lookup"><span data-stu-id="00b09-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="00b09-113">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00b09-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="00b09-114">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="00b09-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="00b09-115">İkinci komut Get-Credential cmdlet 'ini kullanarak bir kimlik bilgisi nesnesi oluşturur ve sonucu $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00b09-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="00b09-116">Komut sizden bir Kullanıcı adı ve parola ister.</span><span class="sxs-lookup"><span data-stu-id="00b09-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="00b09-117">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="00b09-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="00b09-118">Üçüncü komut, $VirtualMachine depolanan sanal makineyi yapılandırmak için **set-AzureRmVMOperatingSystem** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="00b09-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="00b09-119">Dördüncü komut daha sonra kullanmak üzere $SourceVaultId değişkenine bir kaynak Kasası KIMLIĞI atar.</span><span class="sxs-lookup"><span data-stu-id="00b09-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="00b09-120">Komut $SubscriptionId değişkeninde uygun bir değer olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="00b09-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="00b09-121">Beşinci komut, $CertificateStore 01 değişkenine daha sonra kullanmak üzere bir değer atar.</span><span class="sxs-lookup"><span data-stu-id="00b09-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="00b09-122">Altıncı komut, sertifika deposu için bir URL atar.</span><span class="sxs-lookup"><span data-stu-id="00b09-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="00b09-123">Yedinci komutu, $VirtualMachine depolanan sanal makineye bir parola ekler.</span><span class="sxs-lookup"><span data-stu-id="00b09-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="00b09-124">SourceVaultId parametresi Anahtar Kasası belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="00b09-125">Komut, sertifika deposu adını ve sertifikanın URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="00b09-126">Diğer sertifikaların sırlarını eklemek için **Add-AzureRmVMSecret** 'i art arda çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00b09-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="00b09-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00b09-127">PARAMETERS</span></span>

### <span data-ttu-id="00b09-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="00b09-128">-CertificateStore</span></span>
<span data-ttu-id="00b09-129">Windows işletim sistemini çalıştıran sanal makinedeki bir sertifika depolama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="00b09-130">Bu cmdlet, sertifikayı bu parametrenin belirttiği mağazaya ekler.</span><span class="sxs-lookup"><span data-stu-id="00b09-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="00b09-131">Bu parametreyi yalnızca Windows işletim sistemini çalıştıran sanal makineler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00b09-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b09-132">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="00b09-132">-CertificateUrl</span></span>
<span data-ttu-id="00b09-133">Sertifika içeren bir Anahtar Kasası gizliliğini gösteren URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="00b09-134">Sertifika, UTF-8 ile kodlanmış olan aşağıdaki JavaScript nesne gösterimi (JSON) nesnesinin Base64 kodlamasıdır:</span><span class="sxs-lookup"><span data-stu-id="00b09-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="00b09-135">{"Data": " \<Base64-encoded-file\> ", "DataType": " \<file-format\> ", "Password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="00b09-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="00b09-136">Şu anda, veri türü yalnızca. pfx dosyalarını kabul eder.</span><span class="sxs-lookup"><span data-stu-id="00b09-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b09-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="00b09-137">-SourceVaultId</span></span>
<span data-ttu-id="00b09-138">Sanal makineye ekleyebileceğiniz sertifikaları içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="00b09-139">Bu değer, birden çok sertifika ekleme anahtarı olarak da davranır.</span><span class="sxs-lookup"><span data-stu-id="00b09-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="00b09-140">Bu, aynı anahtar kasasından birden çok sertifika eklerken *Sourcevaultid* için aynı değeri kullanabileceğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="00b09-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b09-141">-VM</span><span class="sxs-lookup"><span data-stu-id="00b09-141">-VM</span></span>
<span data-ttu-id="00b09-142">Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b09-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="00b09-143">Sanal makine nesnesi edinmek için [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="00b09-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="00b09-144">Sanal makine nesnesi oluşturmak için [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00b09-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00b09-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b09-145">CommonParameters</span></span>
<span data-ttu-id="00b09-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00b09-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b09-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b09-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b09-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00b09-148">INPUTS</span></span>

### <span data-ttu-id="00b09-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00b09-149">None</span></span>
<span data-ttu-id="00b09-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="00b09-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00b09-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00b09-151">OUTPUTS</span></span>

## <span data-ttu-id="00b09-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00b09-152">NOTES</span></span>

## <span data-ttu-id="00b09-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00b09-153">RELATED LINKS</span></span>

[<span data-ttu-id="00b09-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="00b09-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="00b09-155">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="00b09-155">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="00b09-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="00b09-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
