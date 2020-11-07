---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 05a59e3fd098fb32122cc85a4d39e89cf1fc66aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762524"
---
# <span data-ttu-id="2592a-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2592a-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2592a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2592a-102">SYNOPSIS</span></span>
<span data-ttu-id="2592a-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="2592a-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2592a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2592a-104">SYNTAX</span></span>

### <span data-ttu-id="2592a-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2592a-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2592a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2592a-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2592a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2592a-107">DESCRIPTION</span></span>
<span data-ttu-id="2592a-108">**Remove-AzureKeyVaultCertificateIssuer** cmdlet 'i, bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="2592a-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="2592a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2592a-109">EXAMPLES</span></span>

### <span data-ttu-id="2592a-110">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="2592a-110">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="2592a-111">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2592a-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2592a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2592a-112">PARAMETERS</span></span>

### <span data-ttu-id="2592a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2592a-113">-DefaultProfile</span></span>
<span data-ttu-id="2592a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2592a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2592a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2592a-115">-Force</span></span>
<span data-ttu-id="2592a-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2592a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2592a-117">-InputObject</span></span>
<span data-ttu-id="2592a-118">Sertifikayı verenin nesnesi</span><span class="sxs-lookup"><span data-stu-id="2592a-118">Certificate Issuer Object</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2592a-119">-Name</span></span>
<span data-ttu-id="2592a-120">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2592a-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2592a-121">-PassThru</span></span>
<span data-ttu-id="2592a-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2592a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2592a-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2592a-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2592a-124">-VaultName</span></span>
<span data-ttu-id="2592a-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2592a-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="2592a-126">-Confirm</span></span>
<span data-ttu-id="2592a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2592a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2592a-128">-WhatIf</span></span>
<span data-ttu-id="2592a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2592a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2592a-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2592a-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2592a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2592a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2592a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2592a-132">CommonParameters</span></span>
<span data-ttu-id="2592a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2592a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2592a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2592a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2592a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2592a-135">INPUTS</span></span>

### <span data-ttu-id="2592a-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2592a-136">None</span></span>
<span data-ttu-id="2592a-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2592a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2592a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2592a-138">OUTPUTS</span></span>

### <span data-ttu-id="2592a-139">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="2592a-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2592a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2592a-140">NOTES</span></span>

## <span data-ttu-id="2592a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2592a-141">RELATED LINKS</span></span>

[<span data-ttu-id="2592a-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2592a-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2592a-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2592a-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


