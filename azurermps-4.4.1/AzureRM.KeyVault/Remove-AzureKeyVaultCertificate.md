---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594660"
---
# <span data-ttu-id="f1503-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1503-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="f1503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1503-102">SYNOPSIS</span></span>
<span data-ttu-id="f1503-103">Anahtar kasasından sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1503-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1503-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1503-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1503-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1503-105">DESCRIPTION</span></span>
<span data-ttu-id="f1503-106">**Remove-AzureKeyVaultCertificate** cmdlet 'i anahtar kasadan sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="f1503-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="f1503-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1503-107">EXAMPLES</span></span>

### <span data-ttu-id="f1503-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f1503-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="f1503-109">Bu komut, SelfSigned01 adındaki anahtar kasasına ContosoKV01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1503-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="f1503-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1503-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f1503-111">Bu nedenle, cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="f1503-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f1503-112">Örnek 3: silinen sertifikayı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="f1503-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="f1503-113">Bu komut, ' contoso ' adlı anahtar kasasından ' MyCert ' adlı sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1503-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="f1503-114">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası 'nda önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="f1503-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="f1503-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1503-115">PARAMETERS</span></span>

### <span data-ttu-id="f1503-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f1503-116">-Force</span></span>
<span data-ttu-id="f1503-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f1503-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-118">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="f1503-118">-InRemovedState</span></span>
<span data-ttu-id="f1503-119">Varsa, önceden silinmiş sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1503-119">If present, removes the previously deleted certificate permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1503-120">-Name</span></span>
<span data-ttu-id="f1503-121">Bu cmdlet 'in bir anahtar kasasından kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1503-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="f1503-122">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir sertifikanın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1503-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f1503-123">-PassThru</span></span>
<span data-ttu-id="f1503-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1503-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1503-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f1503-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1503-126">-VaultName</span></span>
<span data-ttu-id="f1503-127">Bu cmdlet 'in sertifikayı kaldırdığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1503-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="f1503-128">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1503-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1503-129">-Confirm</span></span>
<span data-ttu-id="f1503-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1503-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1503-131">-WhatIf</span></span>
<span data-ttu-id="f1503-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1503-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1503-133">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1503-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1503-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1503-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1503-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1503-135">-DefaultProfile</span></span>
<span data-ttu-id="f1503-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1503-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1503-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1503-137">CommonParameters</span></span>
<span data-ttu-id="f1503-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1503-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1503-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1503-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1503-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1503-140">INPUTS</span></span>

## <span data-ttu-id="f1503-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1503-141">OUTPUTS</span></span>

### <span data-ttu-id="f1503-142">Microsoft. Azure. Commands. Keykasa. modeller. Certificatedemeti</span><span class="sxs-lookup"><span data-stu-id="f1503-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="f1503-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1503-143">NOTES</span></span>

## <span data-ttu-id="f1503-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1503-144">RELATED LINKS</span></span>

[<span data-ttu-id="f1503-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1503-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f1503-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1503-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f1503-147">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f1503-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f1503-148">Geri al-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="f1503-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
