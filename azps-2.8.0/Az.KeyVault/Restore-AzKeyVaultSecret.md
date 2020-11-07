---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 9fb79628b123b5d35ae5d55ba31fd07dcbd85775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751629"
---
# <span data-ttu-id="03292-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03292-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="03292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03292-102">SYNOPSIS</span></span>
<span data-ttu-id="03292-103">Yedeklenmiş bir gizli anahtar kasası içinde gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03292-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="03292-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03292-104">SYNTAX</span></span>

### <span data-ttu-id="03292-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03292-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03292-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03292-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03292-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="03292-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03292-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03292-108">DESCRIPTION</span></span>
<span data-ttu-id="03292-109">**Restore-Azanahtarvaultsecret** cmdlet 'i belirtilen anahtar kasası 'nda gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03292-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="03292-110">Bu gizlilik, giriş dosyasındaki yedeklenen gizli dosyaların bir yinelemesidir ve özgün gizlilikle aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="03292-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="03292-111">Anahtar Kasası aynı ada sahip bir gizli anahtar zaten varsa, bu cmdlet özgün gizliliğin üzerine yazılmasında başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="03292-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="03292-112">Yedeklemede bir parolanın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="03292-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="03292-113">Parolayı geri yüklediğiniz tuş Kasası, parolayı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="03292-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="03292-114">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03292-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="03292-115"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="03292-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="03292-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03292-116">EXAMPLES</span></span>

### <span data-ttu-id="03292-117">Örnek 1: yedeklenen gizliliği geri yükleme</span><span class="sxs-lookup"><span data-stu-id="03292-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="03292-118">Bu komut, tüm sürümlerinde, yedekleme. blob adındaki yedekleme dosyasından contoso adlı anahtar kasasına dahil olmak üzere bir parolayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="03292-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="03292-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03292-119">PARAMETERS</span></span>

### <span data-ttu-id="03292-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03292-120">-DefaultProfile</span></span>
<span data-ttu-id="03292-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="03292-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03292-122">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="03292-122">-InputFile</span></span>
<span data-ttu-id="03292-123">Geri yüklenecek parolayı içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03292-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="03292-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03292-124">-InputObject</span></span>
<span data-ttu-id="03292-125">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="03292-125">KeyVault object</span></span>

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

### <span data-ttu-id="03292-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="03292-126">-ResourceId</span></span>
<span data-ttu-id="03292-127">Tuş Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="03292-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="03292-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03292-128">-VaultName</span></span>
<span data-ttu-id="03292-129">Parolayı geri yükleyeceğiniz Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03292-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="03292-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="03292-130">-Confirm</span></span>
<span data-ttu-id="03292-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03292-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03292-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03292-132">-WhatIf</span></span>
<span data-ttu-id="03292-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03292-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03292-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03292-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03292-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03292-135">CommonParameters</span></span>
<span data-ttu-id="03292-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03292-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03292-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03292-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03292-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03292-138">INPUTS</span></span>

### <span data-ttu-id="03292-139">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="03292-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="03292-140">System. String</span><span class="sxs-lookup"><span data-stu-id="03292-140">System.String</span></span>

## <span data-ttu-id="03292-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03292-141">OUTPUTS</span></span>

### <span data-ttu-id="03292-142">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03292-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="03292-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03292-143">NOTES</span></span>

## <span data-ttu-id="03292-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03292-144">RELATED LINKS</span></span>

[<span data-ttu-id="03292-145">Set-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="03292-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="03292-146">Yedek-Aztuş Vaultsecret</span><span class="sxs-lookup"><span data-stu-id="03292-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="03292-147">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="03292-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="03292-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03292-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
