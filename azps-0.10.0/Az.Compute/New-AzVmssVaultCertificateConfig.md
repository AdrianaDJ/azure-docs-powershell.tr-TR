---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936944"
---
# <span data-ttu-id="6f40e-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="6f40e-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="6f40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f40e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f40e-103">Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6f40e-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="6f40e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f40e-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f40e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f40e-105">DESCRIPTION</span></span>
<span data-ttu-id="6f40e-106">**New-AzVmssVaultCertificateConfig** cmdlet 'Inin sanal makine ölçek KÜMESI (VMSS) sanal makinelerine yerleştirilmesi gereken parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f40e-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="6f40e-107">Bu cmdlet 'in çıktısı Add-AzVmssSecret cmdlet ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6f40e-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="6f40e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f40e-108">EXAMPLES</span></span>

### <span data-ttu-id="6f40e-109">Örnek 1: Anahtar Kasası sertifikası yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6f40e-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="6f40e-110">Bu komut, belirtilen sertifika URL 'sinde bulunan mycert adındaki sertifika deposunu kullanan bir Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6f40e-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="6f40e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f40e-111">PARAMETERS</span></span>

### <span data-ttu-id="6f40e-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="6f40e-112">-CertificateStore</span></span>
<span data-ttu-id="6f40e-113">Sanal makinelerde, sertifikanın eklendiği ölçek kümesindeki sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f40e-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="6f40e-114">Bu yalnızca Windows sanal makine ölçek kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6f40e-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="6f40e-115">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="6f40e-115">-CertificateUrl</span></span>
<span data-ttu-id="6f40e-116">Anahtar kasasına depolanan bir sertifikanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f40e-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="6f40e-117">UTF-8 ile kodlanan aşağıdaki JSON nesnesinin Base64 kodlamadır:</span><span class="sxs-lookup"><span data-stu-id="6f40e-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="6f40e-118">{"veriler": " \< Base64 kodlu sertifika \> "," veri türü ":" PFX "," parola ":" \< pfx-dosya-parola \> "}</span><span class="sxs-lookup"><span data-stu-id="6f40e-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f40e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f40e-119">-DefaultProfile</span></span>
<span data-ttu-id="6f40e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f40e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f40e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f40e-121">-Confirm</span></span>
<span data-ttu-id="6f40e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f40e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f40e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f40e-123">-WhatIf</span></span>
<span data-ttu-id="6f40e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f40e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f40e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f40e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f40e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f40e-126">CommonParameters</span></span>
<span data-ttu-id="6f40e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f40e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f40e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f40e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f40e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f40e-129">INPUTS</span></span>

### <span data-ttu-id="6f40e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f40e-130">None</span></span>
<span data-ttu-id="6f40e-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6f40e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f40e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f40e-132">OUTPUTS</span></span>

###  
<span data-ttu-id="6f40e-133">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6f40e-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6f40e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f40e-134">NOTES</span></span>

## <span data-ttu-id="6f40e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f40e-135">RELATED LINKS</span></span>

[<span data-ttu-id="6f40e-136">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="6f40e-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
