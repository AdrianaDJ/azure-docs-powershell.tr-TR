---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936664"
---
# <span data-ttu-id="eee75-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eee75-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="eee75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee75-102">SYNOPSIS</span></span>
<span data-ttu-id="eee75-103">Yedeklenen anahtardan bir Anahtar Kasası 'nda anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eee75-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="eee75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eee75-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eee75-105">DESCRIPTION</span></span>
<span data-ttu-id="eee75-106">**Restore-Azanahtarvaultkey** cmdlet 'i belirtilen anahtar kasası 'nda bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eee75-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="eee75-107">Bu anahtar, giriş dosyasındaki yedeklenen anahtarın bir yinelemesidir ve özgün anahtarla aynı ada sahiptir.</span><span class="sxs-lookup"><span data-stu-id="eee75-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="eee75-108">Anahtar Kasası zaten aynı ada sahip bir anahtara sahipse, özgün anahtarın üzerine yazılması yerine bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="eee75-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="eee75-109">Yedeklemede anahtarın birden çok sürümü varsa, tüm sürümler geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="eee75-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="eee75-110">Anahtarı geri yüklediğiniz tuş Kasası, anahtarı yedeklediğiniz anahtar kasasından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="eee75-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="eee75-111">Ancak, Anahtar Kasası aynı aboneliği kullanmalıdır ve aynı Coğrafya (örneğin Kuzey Amerika) bir Azure bölgesinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eee75-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="eee75-112"> https://azure.microsoft.com/support/trust-center/)Azure bölgelerinin coğrafi olarak eşleştirilmesi Için Microsoft Azure Güven Merkezi 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="eee75-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="eee75-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eee75-113">EXAMPLES</span></span>

### <span data-ttu-id="eee75-114">Örnek 1: Yedeklenen anahtarı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="eee75-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="eee75-115">Bu komut, Backup. blob adındaki yedekleme dosyasındaki Mykeykasa adlı bir anahtar kasasına dahil olmak üzere bir anahtarı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="eee75-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="eee75-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eee75-116">PARAMETERS</span></span>

### <span data-ttu-id="eee75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee75-117">-DefaultProfile</span></span>
<span data-ttu-id="eee75-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eee75-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee75-119">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="eee75-119">-InputFile</span></span>
<span data-ttu-id="eee75-120">Geri yüklenecek anahtarın yedeğini içeren giriş dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee75-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="eee75-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eee75-121">-VaultName</span></span>
<span data-ttu-id="eee75-122">Anahtarın geri yükleneceği anahtar kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee75-122">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee75-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="eee75-123">-Confirm</span></span>
<span data-ttu-id="eee75-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eee75-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee75-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee75-125">-WhatIf</span></span>
<span data-ttu-id="eee75-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eee75-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee75-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eee75-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee75-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee75-128">CommonParameters</span></span>
<span data-ttu-id="eee75-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eee75-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee75-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee75-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee75-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eee75-131">INPUTS</span></span>

### <span data-ttu-id="eee75-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eee75-132">None</span></span>
<span data-ttu-id="eee75-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="eee75-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eee75-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eee75-134">OUTPUTS</span></span>

### <span data-ttu-id="eee75-135">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="eee75-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="eee75-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eee75-136">NOTES</span></span>

## <span data-ttu-id="eee75-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eee75-137">RELATED LINKS</span></span>

[<span data-ttu-id="eee75-138">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="eee75-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="eee75-139">Yedek-Aztuş Vaultkey</span><span class="sxs-lookup"><span data-stu-id="eee75-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="eee75-140">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="eee75-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="eee75-141">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eee75-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

