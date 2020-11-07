---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762718"
---
# <span data-ttu-id="1c541-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c541-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1c541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c541-102">SYNOPSIS</span></span>
<span data-ttu-id="1c541-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="1c541-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c541-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c541-104">SYNTAX</span></span>

### <span data-ttu-id="1c541-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c541-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c541-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c541-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c541-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c541-107">DESCRIPTION</span></span>
<span data-ttu-id="1c541-108">**Remove-AzureKeyVaultCertificateIssuer** cmdlet 'i, bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="1c541-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="1c541-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c541-109">EXAMPLES</span></span>

### <span data-ttu-id="1c541-110">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="1c541-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="1c541-111">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1c541-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1c541-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c541-112">PARAMETERS</span></span>

### <span data-ttu-id="1c541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c541-113">-DefaultProfile</span></span>
<span data-ttu-id="1c541-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1c541-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c541-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1c541-115">-Force</span></span>
<span data-ttu-id="1c541-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1c541-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c541-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c541-117">-InputObject</span></span>
<span data-ttu-id="1c541-118">Sertifikayı verenin nesnesi</span><span class="sxs-lookup"><span data-stu-id="1c541-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="1c541-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c541-119">-Name</span></span>
<span data-ttu-id="1c541-120">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c541-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="1c541-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1c541-121">-PassThru</span></span>
<span data-ttu-id="1c541-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c541-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c541-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1c541-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c541-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1c541-124">-VaultName</span></span>
<span data-ttu-id="1c541-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c541-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1c541-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c541-126">-Confirm</span></span>
<span data-ttu-id="1c541-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c541-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c541-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c541-128">-WhatIf</span></span>
<span data-ttu-id="1c541-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c541-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c541-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c541-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c541-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c541-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c541-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c541-132">CommonParameters</span></span>
<span data-ttu-id="1c541-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c541-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c541-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c541-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c541-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c541-135">INPUTS</span></span>

### <span data-ttu-id="1c541-136">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="1c541-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="1c541-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c541-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1c541-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c541-138">OUTPUTS</span></span>

### <span data-ttu-id="1c541-139">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="1c541-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1c541-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c541-140">NOTES</span></span>

## <span data-ttu-id="1c541-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c541-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c541-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c541-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="1c541-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1c541-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


