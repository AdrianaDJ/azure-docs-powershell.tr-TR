---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098028"
---
# <span data-ttu-id="a0bff-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a0bff-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a0bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0bff-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bff-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="a0bff-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="a0bff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0bff-104">SYNTAX</span></span>

### <span data-ttu-id="a0bff-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0bff-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0bff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0bff-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bff-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0bff-107">DESCRIPTION</span></span>
<span data-ttu-id="a0bff-108">**Remove-Azkeyvaultcertificateıssuer** cmdlet 'i anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="a0bff-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="a0bff-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0bff-109">EXAMPLES</span></span>

### <span data-ttu-id="a0bff-110">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0bff-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="a0bff-111">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0bff-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="a0bff-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0bff-112">PARAMETERS</span></span>

### <span data-ttu-id="a0bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bff-113">-DefaultProfile</span></span>
<span data-ttu-id="a0bff-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0bff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0bff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0bff-115">-Force</span></span>
<span data-ttu-id="a0bff-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a0bff-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0bff-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0bff-117">-InputObject</span></span>
<span data-ttu-id="a0bff-118">Sertifikayı verenin nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0bff-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="a0bff-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0bff-119">-Name</span></span>
<span data-ttu-id="a0bff-120">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0bff-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="a0bff-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0bff-121">-PassThru</span></span>
<span data-ttu-id="a0bff-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0bff-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0bff-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a0bff-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0bff-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0bff-124">-VaultName</span></span>
<span data-ttu-id="a0bff-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0bff-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a0bff-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0bff-126">-Confirm</span></span>
<span data-ttu-id="a0bff-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0bff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bff-128">-WhatIf</span></span>
<span data-ttu-id="a0bff-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0bff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bff-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0bff-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bff-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0bff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bff-132">CommonParameters</span></span>
<span data-ttu-id="a0bff-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0bff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bff-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0bff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bff-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0bff-135">INPUTS</span></span>

### <span data-ttu-id="a0bff-136">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="a0bff-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="a0bff-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0bff-137">OUTPUTS</span></span>

### <span data-ttu-id="a0bff-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="a0bff-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a0bff-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0bff-139">NOTES</span></span>

## <span data-ttu-id="a0bff-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0bff-140">RELATED LINKS</span></span>

[<span data-ttu-id="a0bff-141">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="a0bff-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a0bff-142">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="a0bff-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


