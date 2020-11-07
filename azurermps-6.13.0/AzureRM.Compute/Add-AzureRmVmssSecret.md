---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 423cb695e4dedb978c3902e9c2f2c891a977464c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761984"
---
# <span data-ttu-id="a5bf4-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a5bf4-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="a5bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5bf4-103">Bir VMSS 'ye gizli ekler.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5bf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5bf4-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5bf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="a5bf4-106">**Add-AzureRmVmssSecret** cmdlet 'ı sanal makine ölçek kümesine (VMSS) parola ekler.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a5bf4-107">Gizlilik, bir Azure Anahtar Kasası 'nda depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="a5bf4-108">Anahtar Kasası ile ilgili daha fazla bilgi için [Azure Anahtar Kasası nedir?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="a5bf4-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="a5bf4-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="a5bf4-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="a5bf4-110">Cmdlet 'ler hakkında daha fazla bilgi için bkz: [Azure Anahtar Kasası cmdlet 'leri](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft Developer Network Library veya [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet 'inde.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="a5bf4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5bf4-111">EXAMPLES</span></span>

### <span data-ttu-id="a5bf4-112">Örnek 1: VMSS 'ye gizli ekleme</span><span class="sxs-lookup"><span data-stu-id="a5bf4-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="a5bf4-113">Bu örnek, VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="a5bf4-114">İlk komut, Contosokasası adlı kasada kasa parolası almak için Get-AzureRmKeyVault cmdlet 'ini kullanır ve sonucu $Vault adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="a5bf4-115">İkinci komut **Yeni-AzureRmVmssVaultCertificateConfig** cmdlet 'ini kullanarak, sertifika adlı sertifika deposundan BELIRTILEN sertifika URL 'Sini kullanarak Anahtar Kasası sertifikası yapılandırması oluşturabilir ve sonuçları $CertConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="a5bf4-116">Üçüncü komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a5bf4-117">Dördüncü komut, $Vault ve $CertConfig değişkenlerinde depolanan anahtar kaynak KIMLIĞINI ve kasa sertifikasını kullanarak kasa gizliliğini kullanarak VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="a5bf4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5bf4-118">PARAMETERS</span></span>

### <span data-ttu-id="a5bf4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5bf4-119">-DefaultProfile</span></span>
<span data-ttu-id="a5bf4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5bf4-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a5bf4-121">-SourceVaultId</span></span>
<span data-ttu-id="a5bf4-122">Sanal makineye ekleyebileceğiniz sertifikaları içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="a5bf4-123">Bu değer, birden çok sertifika ekleme anahtarı olarak da davranır.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="a5bf4-124">Bu, aynı anahtar kasasından birden çok sertifika eklerken *Sourcevaultid* parametresinde aynı değeri kullanabileceğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5bf4-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a5bf4-125">-VaultCertificate</span></span>
<span data-ttu-id="a5bf4-126">Sertifika URL 'sini ve sertifika adını içeren kasa **sertifikası** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="a5bf4-127">Bu nesneyi oluşturmak için [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5bf4-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5bf4-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a5bf4-129">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="a5bf4-130">Bu nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5bf4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5bf4-131">-Confirm</span></span>
<span data-ttu-id="a5bf4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bf4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5bf4-133">-WhatIf</span></span>
<span data-ttu-id="a5bf4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5bf4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5bf4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5bf4-136">CommonParameters</span></span>
<span data-ttu-id="a5bf4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5bf4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5bf4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5bf4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5bf4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5bf4-139">INPUTS</span></span>

### <span data-ttu-id="a5bf4-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5bf4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a5bf4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a5bf4-141">System.String</span></span>

### <span data-ttu-id="a5bf4-142">Microsoft. Azure. Management. COMPUTE. model. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="a5bf4-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="a5bf4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5bf4-143">OUTPUTS</span></span>

### <span data-ttu-id="a5bf4-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a5bf4-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a5bf4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5bf4-145">NOTES</span></span>

## <span data-ttu-id="a5bf4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5bf4-146">RELATED LINKS</span></span>

[<span data-ttu-id="a5bf4-147">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="a5bf4-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="a5bf4-148">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a5bf4-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
