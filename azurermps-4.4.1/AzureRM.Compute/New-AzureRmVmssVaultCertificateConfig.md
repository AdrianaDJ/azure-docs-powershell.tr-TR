---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594304"
---
# <span data-ttu-id="b18e1-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="b18e1-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="b18e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b18e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b18e1-103">Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b18e1-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b18e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b18e1-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b18e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b18e1-105">DESCRIPTION</span></span>
<span data-ttu-id="b18e1-106">**New-AzureRmVmssVaultCertificateConfig** cmdlet 'Inin sanal makine ölçek KÜMESI (VMSS) sanal makinelerine yerleştirilmesi gereken parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18e1-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="b18e1-107">Bu cmdlet 'in çıktısı Add-AzureRmVmssSecret cmdlet ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b18e1-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="b18e1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b18e1-108">EXAMPLES</span></span>

### <span data-ttu-id="b18e1-109">Örnek 1: Anahtar Kasası sertifikası yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b18e1-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="b18e1-110">Bu komut, belirtilen sertifika URL 'sinde bulunan mycert adındaki sertifika deposunu kullanan bir Anahtar Kasası sertifikası yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b18e1-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="b18e1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b18e1-111">PARAMETERS</span></span>

### <span data-ttu-id="b18e1-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b18e1-112">-CertificateStore</span></span>
<span data-ttu-id="b18e1-113">Sanal makinelerde, sertifikanın eklendiği ölçek kümesindeki sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18e1-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="b18e1-114">Bu yalnızca Windows sanal makine ölçek kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b18e1-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="b18e1-115">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="b18e1-115">-CertificateUrl</span></span>
<span data-ttu-id="b18e1-116">Anahtar kasasına depolanan bir sertifikanın URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18e1-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="b18e1-117">UTF-8 ile kodlanan aşağıdaki JSON nesnesinin Base64 kodlamadır:</span><span class="sxs-lookup"><span data-stu-id="b18e1-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="b18e1-118">{"Data": " \<Base64-encoded-certificate\> ", "DataType": "PFX", "parola": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="b18e1-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="b18e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18e1-119">-DefaultProfile</span></span>
<span data-ttu-id="b18e1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b18e1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b18e1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b18e1-121">-Confirm</span></span>
<span data-ttu-id="b18e1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b18e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b18e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b18e1-123">-WhatIf</span></span>
<span data-ttu-id="b18e1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b18e1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b18e1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b18e1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b18e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18e1-126">CommonParameters</span></span>
<span data-ttu-id="b18e1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b18e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18e1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18e1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b18e1-129">INPUTS</span></span>

## <span data-ttu-id="b18e1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b18e1-130">OUTPUTS</span></span>

###  
<span data-ttu-id="b18e1-131">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b18e1-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b18e1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b18e1-132">NOTES</span></span>

## <span data-ttu-id="b18e1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b18e1-133">RELATED LINKS</span></span>

[<span data-ttu-id="b18e1-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="b18e1-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
