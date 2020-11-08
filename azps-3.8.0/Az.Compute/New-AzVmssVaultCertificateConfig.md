---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938563"
---
# <span data-ttu-id="795b6-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="795b6-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="795b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="795b6-102">SYNOPSIS</span></span>
<span data-ttu-id="795b6-103">Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="795b6-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="795b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="795b6-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="795b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="795b6-105">DESCRIPTION</span></span>
<span data-ttu-id="795b6-106">**New-AzVmssVaultCertificateConfig** cmdlet 'Inin sanal makine ölçek KÜMESI (VMSS) sanal makinelerine yerleştirilmesi gereken parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="795b6-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="795b6-107">Bu cmdlet 'in çıktısı Add-AzVmssSecret cmdlet ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795b6-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="795b6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="795b6-108">EXAMPLES</span></span>

### <span data-ttu-id="795b6-109">Örnek 1: Anahtar Kasası sertifikası yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="795b6-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="795b6-110">Bu komut, belirtilen sertifika URL 'sinde bulunan mycert adındaki sertifika deposunu kullanan bir Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="795b6-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="795b6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="795b6-111">PARAMETERS</span></span>

### <span data-ttu-id="795b6-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="795b6-112">-CertificateStore</span></span>
<span data-ttu-id="795b6-113">Sanal makinelerde, sertifikanın eklendiği ölçek kümesindeki sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="795b6-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="795b6-114">Bu yalnızca Windows sanal makine ölçek kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="795b6-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="795b6-115">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="795b6-115">-CertificateUrl</span></span>
<span data-ttu-id="795b6-116">Anahtar kasasına depolanan bir sertifikanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="795b6-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="795b6-117">UTF-8 ile kodlanmış olan aşağıdaki JSON nesnesinin Base64 kodlamasıdır: {"Data": " \< base64 kodlu-Certificate \> ", "DataType": "PFX", "parola": " \< pfx-dosya-parola \> "}</span><span class="sxs-lookup"><span data-stu-id="795b6-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="795b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795b6-118">-DefaultProfile</span></span>
<span data-ttu-id="795b6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="795b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="795b6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="795b6-120">-Confirm</span></span>
<span data-ttu-id="795b6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="795b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795b6-122">-WhatIf</span></span>
<span data-ttu-id="795b6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="795b6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="795b6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="795b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795b6-125">CommonParameters</span></span>
<span data-ttu-id="795b6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="795b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795b6-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="795b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795b6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="795b6-128">INPUTS</span></span>

### <span data-ttu-id="795b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="795b6-129">System.String</span></span>

## <span data-ttu-id="795b6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="795b6-130">OUTPUTS</span></span>

### <span data-ttu-id="795b6-131">Microsoft. Azure. Management. COMPUTE. modeller. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="795b6-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="795b6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="795b6-132">NOTES</span></span>

## <span data-ttu-id="795b6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="795b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="795b6-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="795b6-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)