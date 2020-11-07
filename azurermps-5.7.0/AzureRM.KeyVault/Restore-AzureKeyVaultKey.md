---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762854"
---
# <span data-ttu-id="6467c-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="6467c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6467c-102">SYNOPSIS</span></span>
<span data-ttu-id="6467c-103">Yedeklenen anahtardan bir Anahtar Kasası 'nda anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6467c-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6467c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6467c-104">SYNTAX</span></span>

### <span data-ttu-id="6467c-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6467c-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6467c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6467c-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6467c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6467c-107">DESCRIPTION</span></span>
<span data-ttu-id="6467c-108">**Restore-AzureKeyVaultKey** cmdlet 'i belirtilen anahtar kasası 'nda bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6467c-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="6467c-109">Bu anahtar, giriş dosyasındaki yedeklenen anahtarın bir yinelemesidir ve özgün anahtarla aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="6467c-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="6467c-110">Anahtar Kasası zaten aynı ada sahip bir anahtara sahipse, özgün anahtarın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="6467c-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="6467c-111">Yedeklemede anahtarın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="6467c-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="6467c-112">Anahtarı geri yüklediğiniz tuş Kasası, anahtarı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6467c-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="6467c-113">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6467c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6467c-114"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="6467c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6467c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6467c-115">EXAMPLES</span></span>

### <span data-ttu-id="6467c-116">Örnek 1: Yedeklenen anahtarı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="6467c-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="6467c-117">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir anahtar kasasına dahil olmak üzere bir anahtarı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6467c-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="6467c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6467c-118">PARAMETERS</span></span>

### <span data-ttu-id="6467c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6467c-119">-DefaultProfile</span></span>
<span data-ttu-id="6467c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6467c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6467c-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="6467c-121">-InputFile</span></span>
<span data-ttu-id="6467c-122">Geri yüklenecek anahtarın yedeğini içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6467c-122">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="6467c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6467c-123">-InputObject</span></span>
<span data-ttu-id="6467c-124">Tuş Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="6467c-124">KeyVault object</span></span>

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

### <span data-ttu-id="6467c-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6467c-125">-VaultName</span></span>
<span data-ttu-id="6467c-126">Anahtarın geri yükleneceği anahtar kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6467c-126">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="6467c-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6467c-127">-Confirm</span></span>
<span data-ttu-id="6467c-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6467c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6467c-129">-WhatIf</span></span>
<span data-ttu-id="6467c-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6467c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6467c-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6467c-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6467c-132">CommonParameters</span></span>
<span data-ttu-id="6467c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6467c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6467c-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6467c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6467c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6467c-135">INPUTS</span></span>

### <span data-ttu-id="6467c-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6467c-136">None</span></span>
<span data-ttu-id="6467c-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6467c-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6467c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6467c-138">OUTPUTS</span></span>

### <span data-ttu-id="6467c-139">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="6467c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6467c-140">NOTES</span></span>

## <span data-ttu-id="6467c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6467c-141">RELATED LINKS</span></span>

[<span data-ttu-id="6467c-142">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="6467c-143">Yedekleme-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="6467c-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="6467c-145">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6467c-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

