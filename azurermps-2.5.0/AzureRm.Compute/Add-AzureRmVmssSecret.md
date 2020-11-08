---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
ms.openlocfilehash: 9c31442e1242114572540c23049f26715fc3099e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939191"
---
# <span data-ttu-id="b7f49-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="b7f49-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="b7f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f49-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f49-103">Bir VMSS 'ye gizli ekler.</span><span class="sxs-lookup"><span data-stu-id="b7f49-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7f49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7f49-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7f49-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f49-106">**Add-AzureRmVmssSecret** cmdlet 'ı sanal makine ölçek kümesine (VMSS) parola ekler.</span><span class="sxs-lookup"><span data-stu-id="b7f49-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b7f49-107">Gizlilik, bir Azure Anahtar Kasası 'nda depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7f49-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="b7f49-108">Anahtar Kasası ile ilgili daha fazla bilgi için [Azure Anahtar Kasası nedir?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="b7f49-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="b7f49-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b7f49-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="b7f49-110">Cmdlet 'ler hakkında daha fazla bilgi için bkz: [Azure Anahtar Kasası cmdlet 'leri](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft Developer Network Library veya [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet 'inde.</span><span class="sxs-lookup"><span data-stu-id="b7f49-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="b7f49-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7f49-111">EXAMPLES</span></span>

### <span data-ttu-id="b7f49-112">Örnek 1: VMSS 'ye gizli ekleme</span><span class="sxs-lookup"><span data-stu-id="b7f49-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="b7f49-113">Bu örnek, VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="b7f49-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="b7f49-114">İlk komut, Contosokasası adlı kasada kasa parolası almak için Get-AzureRmKeyVault cmdlet 'ini kullanır ve sonucu $Vault adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b7f49-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="b7f49-115">İkinci komut **Yeni-AzureRmVmssVaultCertificateConfig** cmdlet 'ini kullanarak, sertifika adlı sertifika deposundan BELIRTILEN sertifika URL 'Sini kullanarak Anahtar Kasası sertifikası yapılandırması oluşturabilir ve sonuçları $CertConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b7f49-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="b7f49-116">Üçüncü komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b7f49-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b7f49-117">Dördüncü komut, $Vault ve $CertConfig değişkenlerinde depolanan anahtar kaynak KIMLIĞINI ve kasa sertifikasını kullanarak kasa gizliliğini kullanarak VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="b7f49-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="b7f49-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7f49-118">PARAMETERS</span></span>

### <span data-ttu-id="b7f49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f49-119">-DefaultProfile</span></span>
<span data-ttu-id="b7f49-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7f49-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7f49-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b7f49-121">-SourceVaultId</span></span>
<span data-ttu-id="b7f49-122">Sanal makineye ekleyebileceğiniz sertifikaları içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7f49-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="b7f49-123">Bu değer, birden çok sertifika ekleme anahtarı olarak da davranır.</span><span class="sxs-lookup"><span data-stu-id="b7f49-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="b7f49-124">Bu, aynı anahtar kasasından birden çok sertifika eklerken *Sourcevaultid* parametresinde aynı değeri kullanabileceğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b7f49-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f49-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b7f49-125">-VaultCertificate</span></span>
<span data-ttu-id="b7f49-126">Sertifika URL 'sini ve sertifika adını içeren kasa **sertifikası** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7f49-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="b7f49-127">Bu nesneyi oluşturmak için [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7f49-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f49-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b7f49-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b7f49-129">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7f49-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="b7f49-130">Bu nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7f49-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f49-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7f49-131">-Confirm</span></span>
<span data-ttu-id="b7f49-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7f49-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f49-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f49-133">-WhatIf</span></span>
<span data-ttu-id="b7f49-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7f49-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f49-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7f49-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f49-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f49-136">CommonParameters</span></span>
<span data-ttu-id="b7f49-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7f49-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f49-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f49-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f49-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7f49-139">INPUTS</span></span>

### <span data-ttu-id="b7f49-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b7f49-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b7f49-141">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b7f49-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b7f49-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7f49-142">OUTPUTS</span></span>

### <span data-ttu-id="b7f49-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7f49-143">None</span></span>
<span data-ttu-id="b7f49-144">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b7f49-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b7f49-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7f49-145">NOTES</span></span>

## <span data-ttu-id="b7f49-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7f49-146">RELATED LINKS</span></span>

[<span data-ttu-id="b7f49-147">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="b7f49-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="b7f49-148">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b7f49-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)