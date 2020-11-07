---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764652"
---
# <span data-ttu-id="e8084-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8084-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="e8084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8084-102">SYNOPSIS</span></span>
<span data-ttu-id="e8084-103">Bir yedekleme dosyasındaki anahtar kasasındaki sertifikayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e8084-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8084-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8084-104">SYNTAX</span></span>

### <span data-ttu-id="e8084-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8084-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8084-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8084-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8084-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e8084-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8084-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8084-108">DESCRIPTION</span></span>
<span data-ttu-id="e8084-109">**Restore-AzureKeyVaultCertificate** cmdlet 'i, bir yedekleme dosyasından belirtilen anahtar kasasına sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8084-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="e8084-110">Bu sertifika, giriş dosyasındaki yedeklenen sertifikanın bir yinelemesidir ve özgün sertifikayla aynı adı vardır.</span><span class="sxs-lookup"><span data-stu-id="e8084-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="e8084-111">Anahtar Kasası aynı adla bir sertifika içeriyorsa, özgün sertifikanın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="e8084-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="e8084-112">Yedeklemede sertifikanın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e8084-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="e8084-113">Sertifikayı geri yüklediğiniz tuş Kasası, sertifikayı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8084-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="e8084-114">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e8084-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="e8084-115"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="e8084-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="e8084-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8084-116">EXAMPLES</span></span>

### <span data-ttu-id="e8084-117">Örnek 1: yedeklenen sertifikayı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="e8084-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="e8084-118">Bu komut, tüm sürümlerinde, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir Anahtar Kasası olan sertifikayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e8084-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="e8084-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8084-119">PARAMETERS</span></span>

### <span data-ttu-id="e8084-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8084-120">-DefaultProfile</span></span>
<span data-ttu-id="e8084-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8084-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8084-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="e8084-122">-InputFile</span></span>
<span data-ttu-id="e8084-123">Giriş dosyası.</span><span class="sxs-lookup"><span data-stu-id="e8084-123">Input file.</span></span>
<span data-ttu-id="e8084-124">Yedeklenen blob 'u içeren giriş dosyası</span><span class="sxs-lookup"><span data-stu-id="e8084-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="e8084-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8084-125">-InputObject</span></span>
<span data-ttu-id="e8084-126">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="e8084-126">KeyVault object</span></span>

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

### <span data-ttu-id="e8084-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8084-127">-ResourceId</span></span>
<span data-ttu-id="e8084-128">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e8084-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="e8084-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e8084-129">-VaultName</span></span>
<span data-ttu-id="e8084-130">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="e8084-130">Vault name.</span></span>
<span data-ttu-id="e8084-131">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8084-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e8084-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8084-132">-Confirm</span></span>
<span data-ttu-id="e8084-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8084-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8084-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8084-134">-WhatIf</span></span>
<span data-ttu-id="e8084-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8084-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8084-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8084-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8084-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8084-137">CommonParameters</span></span>
<span data-ttu-id="e8084-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8084-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8084-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8084-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8084-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8084-140">INPUTS</span></span>

### <span data-ttu-id="e8084-141">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="e8084-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="e8084-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8084-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e8084-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e8084-143">System.String</span></span>

## <span data-ttu-id="e8084-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8084-144">OUTPUTS</span></span>

### <span data-ttu-id="e8084-145">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8084-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="e8084-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8084-146">NOTES</span></span>

## <span data-ttu-id="e8084-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8084-147">RELATED LINKS</span></span>
