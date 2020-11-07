---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: bd2aaf16d3b9ccaee5bbe7d7eb5c02a4dba9bc21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761369"
---
# <span data-ttu-id="6d2ec-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="6d2ec-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="6d2ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2ec-103">Bir VMSS 'ye gizli ekler.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="6d2ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d2ec-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d2ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d2ec-105">DESCRIPTION</span></span>
<span data-ttu-id="6d2ec-106">**Add-AzVmssSecret** cmdlet 'ı sanal makine ölçek kümesine (VMSS) parola ekler.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6d2ec-107">Gizlilik, bir Azure Anahtar Kasası 'nda depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="6d2ec-108">Anahtar Kasası ile ilgili daha fazla bilgi için [Azure Anahtar Kasası nedir?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="6d2ec-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="6d2ec-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="6d2ec-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="6d2ec-110">Cmdlet 'ler hakkında daha fazla bilgi için bkz: [Azure Anahtar Kasası cmdlet 'leri](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft Developer Network Library veya [set-azkeyvaultsecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet 'inde.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="6d2ec-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d2ec-111">EXAMPLES</span></span>

### <span data-ttu-id="6d2ec-112">Örnek 1: VMSS 'ye gizli ekleme</span><span class="sxs-lookup"><span data-stu-id="6d2ec-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="6d2ec-113">Bu örnek, VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="6d2ec-114">İlk komut, Contosokasası adlı kasada kasa parolası almak için Get-AzKeyVault cmdlet 'ini kullanır ve sonucu $Vault adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="6d2ec-115">İkinci komut **Yeni-AzVmssVaultCertificateConfig** cmdlet 'ini kullanarak, sertifika adlı sertifika deposundan BELIRTILEN sertifika URL 'Sini kullanarak Anahtar Kasası sertifikası yapılandırması oluşturur ve sonuçları $CertConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="6d2ec-116">Üçüncü komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="6d2ec-117">Dördüncü komut, $Vault ve $CertConfig değişkenlerinde depolanan anahtar kaynak KIMLIĞINI ve kasa sertifikasını kullanarak kasa gizliliğini kullanarak VMSS 'ye parola ekler.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="6d2ec-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d2ec-118">PARAMETERS</span></span>

### <span data-ttu-id="6d2ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2ec-119">-DefaultProfile</span></span>
<span data-ttu-id="6d2ec-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d2ec-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6d2ec-121">-SourceVaultId</span></span>
<span data-ttu-id="6d2ec-122">Sanal makineye ekleyebileceğiniz sertifikaları içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="6d2ec-123">Bu değer, birden çok sertifika ekleme anahtarı olarak da davranır.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="6d2ec-124">Bu, aynı anahtar kasasından birden çok sertifika eklerken *Sourcevaultid* parametresinde aynı değeri kullanabileceğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="6d2ec-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d2ec-125">-VaultCertificate</span></span>
<span data-ttu-id="6d2ec-126">Sertifika URL 'sini ve sertifika adını içeren kasa **sertifikası** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="6d2ec-127">Bu nesneyi oluşturmak için [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="6d2ec-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6d2ec-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6d2ec-129">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="6d2ec-130">Bu nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="6d2ec-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d2ec-131">-Confirm</span></span>
<span data-ttu-id="6d2ec-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2ec-133">-WhatIf</span></span>
<span data-ttu-id="6d2ec-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d2ec-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2ec-136">CommonParameters</span></span>
<span data-ttu-id="6d2ec-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2ec-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2ec-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2ec-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d2ec-139">INPUTS</span></span>

### <span data-ttu-id="6d2ec-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6d2ec-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6d2ec-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6d2ec-141">System.String</span></span>

### <span data-ttu-id="6d2ec-142">Microsoft. Azure. Management. COMPUTE. model. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="6d2ec-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="6d2ec-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d2ec-143">OUTPUTS</span></span>

### <span data-ttu-id="6d2ec-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6d2ec-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6d2ec-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d2ec-145">NOTES</span></span>

## <span data-ttu-id="6d2ec-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d2ec-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d2ec-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="6d2ec-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="6d2ec-148">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6d2ec-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)