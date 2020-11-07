---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939775"
---
# <span data-ttu-id="98c99-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="98c99-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="98c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c99-102">SYNOPSIS</span></span>
<span data-ttu-id="98c99-103">Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98c99-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98c99-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c99-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98c99-105">DESCRIPTION</span></span>
<span data-ttu-id="98c99-106">**New-AzureRmVmssVaultCertificateConfig** cmdlet 'Inin sanal makine ölçek KÜMESI (VMSS) sanal makinelerine yerleştirilmesi gereken parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="98c99-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="98c99-107">Bu cmdlet 'in çıktısı Add-AzureRmVmssSecret cmdlet ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="98c99-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="98c99-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98c99-108">EXAMPLES</span></span>

### <span data-ttu-id="98c99-109">Örnek 1: Anahtar Kasası sertifikası yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="98c99-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="98c99-110">Bu komut, belirtilen sertifika URL 'sinde bulunan mycert adındaki sertifika deposunu kullanan bir Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98c99-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="98c99-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98c99-111">PARAMETERS</span></span>

### <span data-ttu-id="98c99-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="98c99-112">-CertificateStore</span></span>
<span data-ttu-id="98c99-113">Sanal makinelerde, sertifikanın eklendiği ölçek kümesindeki sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98c99-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="98c99-114">Bu yalnızca Windows sanal makine ölçek kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="98c99-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="98c99-115">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="98c99-115">-CertificateUrl</span></span>
<span data-ttu-id="98c99-116">Anahtar kasasına depolanan bir sertifikanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98c99-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="98c99-117">UTF-8 ile kodlanan aşağıdaki JSON nesnesinin Base64 kodlamadır:</span><span class="sxs-lookup"><span data-stu-id="98c99-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="98c99-118">{"Data": " \<Base64-encoded-certificate\> ", "DataType": "PFX", "parola": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="98c99-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="98c99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c99-119">-DefaultProfile</span></span>
<span data-ttu-id="98c99-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98c99-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c99-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="98c99-121">-Confirm</span></span>
<span data-ttu-id="98c99-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98c99-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c99-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c99-123">-WhatIf</span></span>
<span data-ttu-id="98c99-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98c99-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c99-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98c99-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c99-126">CommonParameters</span></span>
<span data-ttu-id="98c99-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98c99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c99-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c99-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c99-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98c99-129">INPUTS</span></span>

### <span data-ttu-id="98c99-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="98c99-130">None</span></span>
<span data-ttu-id="98c99-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="98c99-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98c99-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98c99-132">OUTPUTS</span></span>

###  
<span data-ttu-id="98c99-133">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="98c99-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="98c99-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98c99-134">NOTES</span></span>

## <span data-ttu-id="98c99-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98c99-135">RELATED LINKS</span></span>

[<span data-ttu-id="98c99-136">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="98c99-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
