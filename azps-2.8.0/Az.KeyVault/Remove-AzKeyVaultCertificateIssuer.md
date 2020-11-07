---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: bca432cb1747ad8333542ec272ef38c2a6c7598f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751648"
---
# <span data-ttu-id="0a1ea-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0a1ea-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0a1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1ea-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="0a1ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a1ea-104">SYNTAX</span></span>

### <span data-ttu-id="0a1ea-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a1ea-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1ea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0a1ea-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a1ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a1ea-107">DESCRIPTION</span></span>
<span data-ttu-id="0a1ea-108">**Remove-Azkeyvaultcertificateıssuer** cmdlet 'i anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="0a1ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a1ea-109">EXAMPLES</span></span>

### <span data-ttu-id="0a1ea-110">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="0a1ea-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="0a1ea-111">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0a1ea-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a1ea-112">PARAMETERS</span></span>

### <span data-ttu-id="0a1ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1ea-113">-DefaultProfile</span></span>
<span data-ttu-id="0a1ea-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0a1ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a1ea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a1ea-115">-Force</span></span>
<span data-ttu-id="0a1ea-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a1ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a1ea-117">-InputObject</span></span>
<span data-ttu-id="0a1ea-118">Sertifikayı verenin nesnesi</span><span class="sxs-lookup"><span data-stu-id="0a1ea-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a1ea-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a1ea-119">-Name</span></span>
<span data-ttu-id="0a1ea-120">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1ea-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0a1ea-121">-PassThru</span></span>
<span data-ttu-id="0a1ea-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a1ea-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a1ea-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a1ea-124">-VaultName</span></span>
<span data-ttu-id="0a1ea-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1ea-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a1ea-126">-Confirm</span></span>
<span data-ttu-id="0a1ea-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a1ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1ea-128">-WhatIf</span></span>
<span data-ttu-id="0a1ea-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a1ea-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a1ea-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a1ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1ea-132">CommonParameters</span></span>
<span data-ttu-id="0a1ea-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a1ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1ea-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1ea-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a1ea-135">INPUTS</span></span>

### <span data-ttu-id="0a1ea-136">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="0a1ea-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="0a1ea-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a1ea-137">OUTPUTS</span></span>

### <span data-ttu-id="0a1ea-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="0a1ea-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0a1ea-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a1ea-139">NOTES</span></span>

## <span data-ttu-id="0a1ea-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a1ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="0a1ea-141">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="0a1ea-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0a1ea-142">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="0a1ea-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)

