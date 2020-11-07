---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 1a2324012d751de725473b74b71cb80d97d3001e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916248"
---
# <span data-ttu-id="44b68-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="44b68-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="44b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b68-102">SYNOPSIS</span></span>
<span data-ttu-id="44b68-103">Bir yedekleme dosyasındaki anahtar kasasındaki sertifikayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44b68-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="44b68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44b68-104">SYNTAX</span></span>

### <span data-ttu-id="44b68-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44b68-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44b68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="44b68-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44b68-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="44b68-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b68-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="44b68-108">DESCRIPTION</span></span>
<span data-ttu-id="44b68-109">**Restore-Azanahtarvaultcertificate** cmdlet 'i, bir yedekleme dosyasından belirtilen anahtar kasasına sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b68-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="44b68-110">Bu sertifika, giriş dosyasındaki yedeklenen sertifikanın bir yinelemesidir ve özgün sertifikayla aynı adı vardır.</span><span class="sxs-lookup"><span data-stu-id="44b68-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="44b68-111">Anahtar Kasası aynı adla bir sertifika içeriyorsa, özgün sertifikanın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="44b68-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="44b68-112">Yedeklemede sertifikanın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="44b68-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="44b68-113">Sertifikayı geri yüklediğiniz tuş Kasası, sertifikayı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="44b68-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="44b68-114">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="44b68-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="44b68-115"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="44b68-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="44b68-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44b68-116">EXAMPLES</span></span>

### <span data-ttu-id="44b68-117">Örnek 1: yedeklenen sertifikayı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="44b68-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="44b68-118">Bu komut, tüm sürümlerinde, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir Anahtar Kasası olan sertifikayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44b68-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="44b68-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44b68-119">PARAMETERS</span></span>

### <span data-ttu-id="44b68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b68-120">-DefaultProfile</span></span>
<span data-ttu-id="44b68-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44b68-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b68-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="44b68-122">-InputFile</span></span>
<span data-ttu-id="44b68-123">Giriş dosyası.</span><span class="sxs-lookup"><span data-stu-id="44b68-123">Input file.</span></span>
<span data-ttu-id="44b68-124">Yedeklenen blob 'u içeren giriş dosyası</span><span class="sxs-lookup"><span data-stu-id="44b68-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b68-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44b68-125">-InputObject</span></span>
<span data-ttu-id="44b68-126">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="44b68-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44b68-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="44b68-127">-ResourceId</span></span>
<span data-ttu-id="44b68-128">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="44b68-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b68-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="44b68-129">-VaultName</span></span>
<span data-ttu-id="44b68-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="44b68-130">Vault name.</span></span>
<span data-ttu-id="44b68-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b68-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b68-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="44b68-132">-Confirm</span></span>
<span data-ttu-id="44b68-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44b68-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b68-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b68-134">-WhatIf</span></span>
<span data-ttu-id="44b68-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44b68-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b68-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44b68-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b68-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b68-137">CommonParameters</span></span>
<span data-ttu-id="44b68-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44b68-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b68-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b68-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b68-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44b68-140">INPUTS</span></span>

### <span data-ttu-id="44b68-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="44b68-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="44b68-142">System. String</span><span class="sxs-lookup"><span data-stu-id="44b68-142">System.String</span></span>

## <span data-ttu-id="44b68-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44b68-143">OUTPUTS</span></span>

### <span data-ttu-id="44b68-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="44b68-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="44b68-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44b68-145">NOTES</span></span>

## <span data-ttu-id="44b68-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44b68-146">RELATED LINKS</span></span>
