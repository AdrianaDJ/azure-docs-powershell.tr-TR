---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591668"
---
# <span data-ttu-id="ebbc8-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="ebbc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbc8-103">Yedeklenmiş bir gizli anahtar kasası içinde gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebbc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebbc8-104">SYNTAX</span></span>

### <span data-ttu-id="ebbc8-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ebbc8-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbc8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ebbc8-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebbc8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebbc8-107">DESCRIPTION</span></span>
<span data-ttu-id="ebbc8-108">**Restore-AzureKeyVaultSecret** cmdlet 'i belirtilen anahtar kasası 'nda gizli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="ebbc8-109">Bu gizlilik, giriş dosyasındaki yedeklenen gizli dosyaların bir yinelemesidir ve özgün gizlilikle aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="ebbc8-110">Anahtar Kasası aynı ada sahip bir gizli anahtar zaten varsa, bu cmdlet özgün gizliliğin üzerine yazılmasında başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="ebbc8-111">Yedeklemede bir parolanın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="ebbc8-112">Parolayı geri yüklediğiniz tuş Kasası, parolayı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="ebbc8-113">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ebbc8-114"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ebbc8-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebbc8-115">EXAMPLES</span></span>

### <span data-ttu-id="ebbc8-116">Örnek 1: yedeklenen gizliliği geri yükleme</span><span class="sxs-lookup"><span data-stu-id="ebbc8-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="ebbc8-117">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı yedekleme dosyasından, tüm sürümleri dahil bir parolayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ebbc8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebbc8-118">PARAMETERS</span></span>

### <span data-ttu-id="ebbc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbc8-119">-DefaultProfile</span></span>
<span data-ttu-id="ebbc8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ebbc8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebbc8-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="ebbc8-121">-InputFile</span></span>
<span data-ttu-id="ebbc8-122">Geri yüklenecek parolayı içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebbc8-123">-InputObject</span></span>
<span data-ttu-id="ebbc8-124">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="ebbc8-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ebbc8-125">-VaultName</span></span>
<span data-ttu-id="ebbc8-126">Parolayı geri yükleyeceğiniz Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc8-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ebbc8-127">-Confirm</span></span>
<span data-ttu-id="ebbc8-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebbc8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbc8-129">-WhatIf</span></span>
<span data-ttu-id="ebbc8-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbc8-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebbc8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbc8-132">CommonParameters</span></span>
<span data-ttu-id="ebbc8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbc8-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbc8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbc8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebbc8-135">INPUTS</span></span>

### <span data-ttu-id="ebbc8-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ebbc8-136">None</span></span>
<span data-ttu-id="ebbc8-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ebbc8-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebbc8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebbc8-138">OUTPUTS</span></span>

### <span data-ttu-id="ebbc8-139">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ebbc8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebbc8-140">NOTES</span></span>

## <span data-ttu-id="ebbc8-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebbc8-141">RELATED LINKS</span></span>

[<span data-ttu-id="ebbc8-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="ebbc8-143">Yedekleme-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="ebbc8-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="ebbc8-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ebbc8-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

